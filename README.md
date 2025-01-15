#### The full implementation:
# On the effect of the average clustering coefficient on topology-based link prediction

This repository is divided into two sections. The _Experiments_ directory contains the source code for experiments 1 to 3. These experiments utilize NetworkX. The _OBGL_ directory is a fork of [SEAL_OGB](https://github.com/facebookresearch/SEAL_OGB) with an additional implementation for the Heterogeneity Index, Homogeneity Index and the Jaccard Index. This set of evaluation utilizes PyTorch.
Our article can be viewed and downloaded from [https://arxiv.org/abs/2501.06721](https://arxiv.org/abs/2501.06721).
#### A GPU is not required nor used for these experiments. Linux OS might be necessary.
## Experiments
*LinkPrediction.ipynb*: calculates the average clustering coefficient and the link prediction AUC for a given graph using Heterogeneity Index, Homogeneity Index and the Jaccard Index \
*Exp1-2_InflectionRunner.ipynb*: Calculates the average clustering coefficient, Jaccard Index, Heterogeneity Index, Homogeneity Index for different link formation probabilities $d$ until the threshold is found.\
*Exp3_GraphOrder.ipynb*: Calculates the boundary for different graph sizes\
*rafie_model.ipynb*: Alters a given graph $G$ with probability $d$, increasing its average clustering coefficient while maintaining heterogeneity\
*OGBConvert.ipynb*: Converts OGBL npy objects to CSV edge list for link prediction

## OBGL
This section is a fork of [SEAL_OGB](https://github.com/facebookresearch/SEAL_OGB). To use it, execute the following command:
```
python seal_link_pred.py --use_heuristic CN --dataset ogbl-ppa
```
You can change the value for the *--use_heuristic* argument with `JC` for Jaccard Index, `HI` for Heterogeneity Index, and `HO` for Homogeneity Index. Moreover, you can change the value for `--dataset` with existing datasets in [this link](https://ogb.stanford.edu/docs/linkprop/) (note that you should use undirected, unweighted graphs).

## Citation
If you use our work in your research, please cite it as:
```
@misc{rafiepour2025effectaverageclusteringcoefficient,
      title={On the effect of the average clustering coefficient on topology-based link prediction in featureless graphs}, 
      author={Mehrdad Rafiepour and S. Mehdi Vahidipour},
      year={2025},
      eprint={2501.06721},
      archivePrefix={arXiv},
      primaryClass={cs.SI},
      url={https://arxiv.org/abs/2501.06721}, 
}
```
## License
OBGL directory:
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)\
Experiments Directory:
 [![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)<br>
   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.

