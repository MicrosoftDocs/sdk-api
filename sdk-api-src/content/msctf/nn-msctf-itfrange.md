---
UID: NN:msctf.ITfRange
title: ITfRange
author: windows-sdk-content
description: The ITfRange interface is used by text services and applications to reference and manipulate text within a given context. The interface ID is IID_ITfRange.
old-location: tsf\itfrange.htm
old-project: TSF
ms.assetid: b8889f7d-3228-4ecc-8d24-c04234d3101e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITfRange, ITfRange interface [Text Services Framework], ITfRange interface [Text Services Framework],described, _tsf_itfrange_ref, msctf/ITfRange, tsf.itfrange
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msctf.h
req.include-header: 
req.redist: TSF 1.0 on Windows 2000 Professional
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
tech.root: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfRange
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfRange interface


## -description


The <b>ITfRange</b> interface is used by text services and applications to reference and manipulate text within a given context. The interface ID is IID_ITfRange.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfRange</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfRange</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/b286266c-d6cf-4291-b4b2-24d5a3d4e1ad">AdjustForInsert</a>
</td>
<td align="left" width="63%">
Expands or contracts a range for text insertion.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b85012f-b090-4c91-b29c-b2470ff63ab6">Clone</a>
</td>
<td align="left" width="63%">
Duplicates the range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/657b1ffe-a958-4eb0-8014-6c068711b809">Collapse</a>
</td>
<td align="left" width="63%">
Empties the range by moving its start anchor and end anchor to the same position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/23841f07-f2ea-4365-a8cb-128c4fb210ab">CompareEnd</a>
</td>
<td align="left" width="63%">
Compares the position of this range end anchor to an anchor in another range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b84375ec-e00a-4cb3-97b7-f10688814968">CompareStart</a>
</td>
<td align="left" width="63%">
Compares the position of this range start anchor to an anchor in another range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c3ba1424-f6c9-41f1-b815-4c315bfba868">GetContext</a>
</td>
<td align="left" width="63%">
Obtains the context object to which the range belongs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ff8c4f60-76d5-422d-9d23-584e8eb5f1a1">GetEmbedded</a>
</td>
<td align="left" width="63%">
Obtains content corresponding to a TF_CHAR_EMBEDDED character in the text stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8da4cb21-7097-4ba9-a63b-3699ef267776">GetFormattedText</a>
</td>
<td align="left" width="63%">
Obtains specially formatted content contained within a range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7569b9dd-869f-49a6-ad0f-c2d9b5f0ae70">GetGravity</a>
</td>
<td align="left" width="63%">
Obtains the gravity of the anchors in the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b38a8de3-947f-469c-9f0d-f0482ea86884">GetText</a>
</td>
<td align="left" width="63%">
Obtains content covered by this range of text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95b8622d-c934-4293-abb4-9eface451be5">InsertEmbedded</a>
</td>
<td align="left" width="63%">
Inserts an object at the location of the start anchor of the range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4cc720c1-acc1-445e-830e-91135fdfeeed">IsEmpty</a>
</td>
<td align="left" width="63%">
Verifies that the range is empty, because the start anchor and end anchor occupy the same position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/03b87230-457f-4483-a183-d8a8cc7cead4">IsEqualEnd</a>
</td>
<td align="left" width="63%">
Verifies that the end anchor of this range matches an anchor of another specified range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/562c2821-9522-4fb5-ae15-4430cd2711c6">IsEqualStart</a>
</td>
<td align="left" width="63%">
Verifies that the start anchor of this range matches an anchor of another specified range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f8be0458-cd14-471d-a138-0730f87374e0">SetGravity</a>
</td>
<td align="left" width="63%">
Sets the gravity of the anchors in the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/797d96a1-0250-4e8d-a4bd-31152fd6eca7">SetText</a>
</td>
<td align="left" width="63%">
Replaces content covered by the range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1debec6d-f98f-45a4-aaa8-99b61f3583ef">ShiftEnd</a>
</td>
<td align="left" width="63%">
Moves the end anchor of the range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cda2282f-3d3c-4763-9892-b889b29963a6">ShiftEndRegion</a>
</td>
<td align="left" width="63%">
Moves the end anchor into an adjacent region.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/27595909-025b-46c9-bd6f-2e64a720c97c">ShiftEndToRange</a>
</td>
<td align="left" width="63%">
Moves the end anchor of this range to an anchor within another range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f9f983b1-a5fa-4857-b73c-b879c566d6f6">ShiftStart</a>
</td>
<td align="left" width="63%">
Moves the start anchor of the range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6e16112a-0cfe-41be-9d9c-4cbcde898c3f">ShiftStartRegion</a>
</td>
<td align="left" width="63%">
Moves the start anchor into an adjacent region.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e3e40a0-71ba-4abf-ac99-99d66856746c">ShiftStartToRange</a>
</td>
<td align="left" width="63%">
Moves the start anchor of this range to an anchor within another range.

</td>
</tr>
</table> 


## -remarks



The TSF manager implements this interface. For more information about ranges, anchors, embedded objects, and other text properties used by TSF, see <a href="https://msdn.microsoft.com/7488e29e-3409-4db3-98b4-f3438ad7c94e">Ranges</a>, <a href="https://msdn.microsoft.com/44cb22b5-707b-4f21-b986-5258ed273543">Embedded Objects</a>, and other topics within <a href="https://msdn.microsoft.com/383a7c31-389b-4f8a-a5eb-552493bef640">Using Text Services Framework</a>.


#### Examples

Once an <a href="https://msdn.microsoft.com/b1eb5782-13e3-4cbb-8c37-ce7219d1e838">ITfComposition</a> composition object is instantiated, a pointer to an <b>ITfRange</b> interface pointer can be obtained by calling the <a href="https://msdn.microsoft.com/14a726c3-6531-4d49-9f22-20460be02b81">ITfComposition::GetRange</a> method, as shown in the following code example.

<div class="code"></div>
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT         hr;
ITfComposition  *pComposition;
ITfRange        *pRange;
WCHAR           *achBuffer[64];  // Buffer to receive text. 
ULONG           cch;

hr = pComposition-&gt;GetRange(&amp;pRange);
if(SUCCEEDED(hr))
{
    // Loop to scan text: 

    do
    {
        cch = ARRAYSIZE(achBuffer);
        hr = pRange-&gt;GetText(ec, TF_TF_MOVESTART | TF_TF_IGNOREEND, achBuffer, cch, &amp;cch);
        if(SUCCEEDED(hr))
        {
            // Do something with the text. 

            pRange-&gt;Release();
        }
    }
    while (cch == ARRAYSIZE(achBuffer));

    pComposition-&gt;Release();
}
</pre>
</td>
</tr>
</table></span></div>
A pointer to a current <b>ITfRange</b> object can be obtained from the &lt;range&gt; element of the <a href="https://msdn.microsoft.com/c844a6d1-b3b9-49cf-83a6-1ee8b3bd2d54">TF_SELECTION</a> structure.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/3d9da4f2-ceb9-4abc-8979-d3756d948a57">Compositions</a>



<a href="https://msdn.microsoft.com/44cb22b5-707b-4f21-b986-5258ed273543">Embedded Objects</a>



<a href="https://msdn.microsoft.com/b1eb5782-13e3-4cbb-8c37-ce7219d1e838">ITfComposition
      </a>



<a href="https://msdn.microsoft.com/14a726c3-6531-4d49-9f22-20460be02b81">ITfComposition::GetRange
      </a>



<a href="_COM_IUnknown">IUnknown</a>



<a href="https://msdn.microsoft.com/7488e29e-3409-4db3-98b4-f3438ad7c94e">Ranges</a>



<a href="https://msdn.microsoft.com/c844a6d1-b3b9-49cf-83a6-1ee8b3bd2d54">TF_SELECTION
      </a>



<a href="https://msdn.microsoft.com/383a7c31-389b-4f8a-a5eb-552493bef640">Using Text Services Framework</a>
 

 

