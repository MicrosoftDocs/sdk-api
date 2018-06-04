---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ITextRange2::Linearize


## -description


Translates the built-up math, ruby, and other inline objects in this range to linearized form.


## -parameters




### -param Flags [in]

Type: <b>long</b>

A combination of the following flags.

<a id="tomMathAlphabetics"></a>
<a id="tommathalphabetics"></a>
<a id="TOMMATHALPHABETICS"></a>


#### tomMathAlphabetics

<a id="tomMathBuildDownOutermost"></a>
<a id="tommathbuilddownoutermost"></a>
<a id="TOMMATHBUILDDOWNOUTERMOST"></a>


#### tomMathBuildDownOutermost

<a id="tomMathBuildUpArgOrZone"></a>
<a id="tommathbuildupargorzone"></a>
<a id="TOMMATHBUILDUPARGORZONE"></a>


#### tomMathBuildUpArgOrZone

<a id="tomMathRemoveOutermost"></a>
<a id="tommathremoveoutermost"></a>
<a id="TOMMATHREMOVEOUTERMOST"></a>


#### tomMathRemoveOutermost

<a id="tomPlain"></a>
<a id="tomplain"></a>
<a id="TOMPLAIN"></a>


#### tomPlain

<a id="__tomTeX"></a>
<a id="__tomtex"></a>
<a id="__TOMTEX"></a>


#### tomTeX


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
</table>
 




## -remarks



If the linearization is successful, the originally selected range is replaced by the linearized version. 

If the <b>tomMathRemoveOutermost</b> or <b>tomMathBuildDownOutermost</b> build down mode is specified, the build down operation can be affected by the <a href="tomconstants.htm">tomMathChangeMask</a> values.

 The main purpose of these build-down modes is to facilitate transformations of the build-up math object as exposed by math context menus. 


For example, to convert a stacked fraction to a linear fraction as in
(a+b/c)/(u+x/y)→((a+b/c))⁄((u+x/y)),
parentheses must be inserted; otherwise, you get a transformation
that looks incorrect, as in (a+b/c)/(u+x/y)→(a+b/c)⁄(u+x/y),
even though internally the linear fraction still has the original numerator and denominator. 

The build-down process automatically inserts the parentheses, because the linear format for this case has parentheses, and the special change is made to replace the stacked-fraction operator U+002F by the linear fraction operator U+2215. Build up doesn't discard the parentheses for U+2215, but it does for U+002F.






## -see-also




<a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a>



<a href="https://msdn.microsoft.com/b6382f09-126e-4107-a4b9-288777549181">ITextRange2::BuildUpMath</a>
 

 

