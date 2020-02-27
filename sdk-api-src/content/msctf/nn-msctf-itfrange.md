---
UID: NN:msctf.ITfRange
title: ITfRange (msctf.h)
description: The ITfRange interface is used by text services and applications to reference and manipulate text within a given context. The interface ID is IID_ITfRange.
old-location: tsf\itfrange.htm
tech.root: TSF
ms.assetid: b8889f7d-3228-4ecc-8d24-c04234d3101e
ms.date: 12/05/2018
ms.keywords: ITfRange, ITfRange interface [Text Services Framework], ITfRange interface [Text Services Framework],described, _tsf_itfrange_ref, msctf/ITfRange, tsf.itfrange
f1_keywords:
- msctf/ITfRange
dev_langs:
- c++
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- msctf.dll
api_name:
- ITfRange
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfRange interface


## -description


The <b>ITfRange</b> interface is used by text services and applications to reference and manipulate text within a given context. The interface ID is IID_ITfRange.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfRange</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfRange</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfRange</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfrange-adjustforinsert">AdjustForInsert</a>
</td>
<td align="left" width="63%">
Expands or contracts a range for text insertion.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfrange-clone">Clone</a>
</td>
<td align="left" width="63%">
Duplicates the range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfrange-collapse">Collapse</a>
</td>
<td align="left" width="63%">
Empties the range by moving its start anchor and end anchor to the same position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfrange-compareend">CompareEnd</a>
</td>
<td align="left" width="63%">
Compares the position of this range end anchor to an anchor in another range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfrange-comparestart">CompareStart</a>
</td>
<td align="left" width="63%">
Compares the position of this range start anchor to an anchor in another range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfrange-getcontext">GetContext</a>
</td>
<td align="left" width="63%">
Obtains the context object to which the range belongs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfrange-getembedded">GetEmbedded</a>
</td>
<td align="left" width="63%">
Obtains content corresponding to a TF_CHAR_EMBEDDED character in the text stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfrange-getformattedtext">GetFormattedText</a>
</td>
<td align="left" width="63%">
Obtains specially formatted content contained within a range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfrange-getgravity">GetGravity</a>
</td>
<td align="left" width="63%">
Obtains the gravity of the anchors in the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfrange-gettext">GetText</a>
</td>
<td align="left" width="63%">
Obtains content covered by this range of text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfrange-insertembedded">InsertEmbedded</a>
</td>
<td align="left" width="63%">
Inserts an object at the location of the start anchor of the range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfrange-isempty">IsEmpty</a>
</td>
<td align="left" width="63%">
Verifies that the range is empty, because the start anchor and end anchor occupy the same position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfrange-isequalend">IsEqualEnd</a>
</td>
<td align="left" width="63%">
Verifies that the end anchor of this range matches an anchor of another specified range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfrange-isequalstart">IsEqualStart</a>
</td>
<td align="left" width="63%">
Verifies that the start anchor of this range matches an anchor of another specified range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfrange-setgravity">SetGravity</a>
</td>
<td align="left" width="63%">
Sets the gravity of the anchors in the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfrange-settext">SetText</a>
</td>
<td align="left" width="63%">
Replaces content covered by the range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfrange-shiftend">ShiftEnd</a>
</td>
<td align="left" width="63%">
Moves the end anchor of the range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfrange-shiftendregion">ShiftEndRegion</a>
</td>
<td align="left" width="63%">
Moves the end anchor into an adjacent region.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfrange-shiftendtorange">ShiftEndToRange</a>
</td>
<td align="left" width="63%">
Moves the end anchor of this range to an anchor within another range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfrange-shiftstart">ShiftStart</a>
</td>
<td align="left" width="63%">
Moves the start anchor of the range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfrange-shiftstartregion">ShiftStartRegion</a>
</td>
<td align="left" width="63%">
Moves the start anchor into an adjacent region.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfrange-shiftstarttorange">ShiftStartToRange</a>
</td>
<td align="left" width="63%">
Moves the start anchor of this range to an anchor within another range.

</td>
</tr>
</table> 


## -remarks



The TSF manager implements this interface. For more information about ranges, anchors, embedded objects, and other text properties used by TSF, see <a href="https://docs.microsoft.com/windows/desktop/TSF/ranges">Ranges</a>, <a href="https://docs.microsoft.com/windows/desktop/TSF/embedded-objects">Embedded Objects</a>, and other topics within <a href="https://docs.microsoft.com/windows/desktop/TSF/using-text-services-framework">Using Text Services Framework</a>.


#### Examples

Once an <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfcomposition">ITfComposition</a> composition object is instantiated, a pointer to an <b>ITfRange</b> interface pointer can be obtained by calling the <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcomposition-getrange">ITfComposition::GetRange</a> method, as shown in the following code example.

<div class="code"></div>

```cpp

HRESULT         hr;
ITfComposition  *pComposition;
ITfRange        *pRange;
WCHAR           *achBuffer[64];  // Buffer to receive text. 
ULONG           cch;

hr = pComposition->GetRange(&pRange);
if(SUCCEEDED(hr))
{
    // Loop to scan text: 

    do
    {
        cch = ARRAYSIZE(achBuffer);
        hr = pRange->GetText(ec, TF_TF_MOVESTART | TF_TF_IGNOREEND, achBuffer, cch, &cch);
        if(SUCCEEDED(hr))
        {
            // Do something with the text. 

            pRange->Release();
        }
    }
    while (cch == ARRAYSIZE(achBuffer));

    pComposition->Release();
}

```


A pointer to a current <b>ITfRange</b> object can be obtained from the &lt;range&gt; element of the <a href="https://docs.microsoft.com/windows/desktop/api/msctf/ns-msctf-tf_selection">TF_SELECTION</a> structure.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/TSF/compositions">Compositions</a>



<a href="https://docs.microsoft.com/windows/desktop/TSF/embedded-objects">Embedded Objects</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfcomposition">ITfComposition
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcomposition-getrange">ITfComposition::GetRange
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/windows/desktop/TSF/ranges">Ranges</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/ns-msctf-tf_selection">TF_SELECTION
      </a>



<a href="https://docs.microsoft.com/windows/desktop/TSF/using-text-services-framework">Using Text Services Framework</a>
 

 

