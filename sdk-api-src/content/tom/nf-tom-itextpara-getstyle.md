---
UID: NF:tom.ITextPara.GetStyle
title: ITextPara::GetStyle (tom.h)
description: Retrieves the style handle to the paragraphs in the specified range.
helpviewer_keywords: ["GetStyle","GetStyle method [Windows Controls]","GetStyle method [Windows Controls]","ITextPara interface","ITextPara interface [Windows Controls]","GetStyle method","ITextPara.GetStyle","ITextPara::GetStyle","_win32_ITextPara_GetStyle","_win32_ITextPara_GetStyle_cpp","controls.ITextPara_GetStyle","controls._win32_ITextPara_GetStyle","tom/ITextPara::GetStyle"]
old-location: controls\ITextPara_GetStyle.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\itextpara\itextparagetstyle.htm
ms.date: 12/05/2018
ms.keywords: GetStyle, GetStyle method [Windows Controls], GetStyle method [Windows Controls],ITextPara interface, ITextPara interface [Windows Controls],GetStyle method, ITextPara.GetStyle, ITextPara::GetStyle, _win32_ITextPara_GetStyle, _win32_ITextPara_GetStyle_cpp, controls.ITextPara_GetStyle, controls._win32_ITextPara_GetStyle, tom/ITextPara::GetStyle
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msftedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextPara::GetStyle
 - tom/ITextPara::GetStyle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextPara.GetStyle
---

# ITextPara::GetStyle


## -description

Retrieves the style handle to the paragraphs in the specified range.

## -parameters

### -param pValue

Type: <b>long*</b>

The paragraph style handle. For more information, see the Remarks.

## -returns

Type: <b>HRESULT</b>

If <b>ITextPara::GetStyle</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Value</b></dt>
</dl>
</td>
<td width="60%">
Meaning

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_RELEASED</b></dt>
</dl>
</td>
<td width="60%">
The paragraph formatting object is attached to a range that has been deleted.

</td>
</tr>
</table>

## -remarks

The Text Object Model (TOM) version 1.0 has no way to specify the meanings of user-defined style handles. They depend on other facilities of the text system implementing TOM. Negative style handles are reserved for built-in character and paragraph styles. Currently defined values are listed in the following table. For a description of the following styles, see the Microsoft Word documentation.

<table class="clsStd">
<tr>
<th>Style </th>
<th>Value</th>
<th>Style</th>
<th>Value</th>
</tr>
<tr>
<td>StyleNormal</td>
<td>–1</td>
<td>StyleTableofAuthorities</td>
<td>–45</td>
</tr>
<tr>
<td>StyleHeading1</td>
<td>–2</td>
<td>StyleMacroText</td>
<td>–46</td>
</tr>
<tr>
<td>StyleHeading2</td>
<td>–3</td>
<td>StyleTOAHeading</td>
<td>–47</td>
</tr>
<tr>
<td>StyleHeading3</td>
<td>–4</td>
<td>StyleList</td>
<td>–48</td>
</tr>
<tr>
<td>StyleHeading4</td>
<td>–5</td>
<td>StyleListBullet</td>
<td>–49</td>
</tr>
<tr>
<td>StyleHeading5</td>
<td>–6</td>
<td>StyleListNumber</td>
<td>–50</td>
</tr>
<tr>
<td>StyleHeading6</td>
<td>–7</td>
<td>StyleList2</td>
<td>–51</td>
</tr>
<tr>
<td>StyleHeading7</td>
<td>–8</td>
<td>StyleList3</td>
<td>–52</td>
</tr>
<tr>
<td>StyleHeading8</td>
<td>–9</td>
<td>StyleList4</td>
<td>–53</td>
</tr>
<tr>
<td>StyleHeading9</td>
<td>–10</td>
<td>StyleList5</td>
<td>–54</td>
</tr>
<tr>
<td>StyleIndex1</td>
<td>–11</td>
<td>StyleListBullet2</td>
<td>–55</td>
</tr>
<tr>
<td>StyleIndex2</td>
<td>–12</td>
<td>StyleListBullet3</td>
<td>–56</td>
</tr>
<tr>
<td>StyleIndex3</td>
<td>–13</td>
<td>StyleListBullet4</td>
<td>–57</td>
</tr>
<tr>
<td>StyleIndex4</td>
<td>–14</td>
<td>StyleListBullet5</td>
<td>–58</td>
</tr>
<tr>
<td>StyleIndex5</td>
<td>–15</td>
<td>StyleListNumber2</td>
<td>–59</td>
</tr>
<tr>
<td>StyleIndex6</td>
<td>–16</td>
<td>StyleListNumber3</td>
<td>–60</td>
</tr>
<tr>
<td>StyleIndex7</td>
<td>–17</td>
<td>StyleListNumber4</td>
<td>–61</td>
</tr>
<tr>
<td>StyleIndex8</td>
<td>–18</td>
<td>StyleListNumber5</td>
<td>–62</td>
</tr>
<tr>
<td>StyleIndex9</td>
<td>–19</td>
<td>StyleTitle</td>
<td>–63</td>
</tr>
<tr>
<td>StyleTOC1</td>
<td>–20</td>
<td>StyleClosing</td>
<td>–64</td>
</tr>
<tr>
<td>StyleTOC2</td>
<td>–21</td>
<td>StyleSignature</td>
<td>–65</td>
</tr>
<tr>
<td>StyleTOC3</td>
<td>–22</td>
<td>StyleDefaultParagraphFont</td>
<td>–66</td>
</tr>
<tr>
<td>StyleTOC4</td>
<td>–23</td>
<td>StyleBodyText</td>
<td>–67</td>
</tr>
<tr>
<td>StyleTOC5</td>
<td>–24</td>
<td>StyleBodyTextIndent</td>
<td>–68</td>
</tr>
<tr>
<td>StyleTOC6</td>
<td>–25</td>
<td>StyleListContinue</td>
<td>–69</td>
</tr>
<tr>
<td>StyleTOC7</td>
<td>–26</td>
<td>StyleListContinue2</td>
<td>–70</td>
</tr>
<tr>
<td>StyleTOC8</td>
<td>–27</td>
<td>StyleListContinue3</td>
<td>–71</td>
</tr>
<tr>
<td>StyleTOC9</td>
<td>–28</td>
<td>StyleListContinue4</td>
<td>–72</td>
</tr>
<tr>
<td>StyleNormalIndent</td>
<td>–29</td>
<td>StyleListContinue5</td>
<td>–73</td>
</tr>
<tr>
<td>StyleFootnoteText</td>
<td>–30</td>
<td>StyleMessageHeader</td>
<td>–74</td>
</tr>
<tr>
<td>StyleAnnotationText</td>
<td>–31</td>
<td>StyleSubtitle</td>
<td>–75</td>
</tr>
<tr>
<td>StyleHeader</td>
<td>–32</td>
<td>StyleSalutation</td>
<td>–76</td>
</tr>
<tr>
<td>StyleFooter</td>
<td>–33</td>
<td>StyleDate</td>
<td>–77</td>
</tr>
<tr>
<td>StyleIndexHeading</td>
<td>–34</td>
<td>StyleBodyTextFirstIndent</td>
<td>–78</td>
</tr>
<tr>
<td>StyleCaption</td>
<td>–35</td>
<td>StyleBodyTextFirstIndent2</td>
<td>–79</td>
</tr>
<tr>
<td>StyleTableofFigures</td>
<td>–36</td>
<td>StyleNoteHeading</td>
<td>–80</td>
</tr>
<tr>
<td>StyleEnvelopeAddress</td>
<td>–37</td>
<td>StyleBodyText2</td>
<td>–81</td>
</tr>
<tr>
<td>StyleEnvelopeReturn</td>
<td>–38</td>
<td>StyleBodyText3</td>
<td>–82</td>
</tr>
<tr>
<td>StyleFootnoteReference</td>
<td>–39</td>
<td>StyleBodyTextIndent2</td>
<td>–83</td>
</tr>
<tr>
<td>StyleAnnotationReference</td>
<td>–40</td>
<td>StyleBodyTextIndent3</td>
<td>–84</td>
</tr>
<tr>
<td>StyleLineNumber</td>
<td>–41</td>
<td>StyleBlockQuotation</td>
<td>–85</td>
</tr>
<tr>
<td>StylePageNumber</td>
<td>–42</td>
<td>StyleHyperlink</td>
<td>–86</td>
</tr>
<tr>
<td>StyleEndnoteReference</td>
<td>–43</td>
<td>StyleHyperlinkFollowed</td>
<td>–87</td>
</tr>
<tr>
<td>StyleEndnoteText</td>
<td>–44</td>
<td> 
						</td>
<td> 
						</td>
</tr>
</table>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a>



<b>Reference</b>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-setstyle">SetStyle</a>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>