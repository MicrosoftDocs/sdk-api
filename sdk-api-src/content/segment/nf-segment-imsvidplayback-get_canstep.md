---
UID: NF:segment.IMSVidPlayback.get_CanStep
title: IMSVidPlayback::get_CanStep
author: windows-sdk-content
description: The get_CanStep method queries whether the input source can step frame by frame.
old-location: mstv\imsvidplayback_get_canstep.htm
old-project: mstv
ms.assetid: 41aad247-1f04-4245-89df-8ac527926307
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IMSVidPlayback interface [Microsoft TV Technologies],get_CanStep method, IMSVidPlayback.get_CanStep, IMSVidPlayback::get_CanStep, IMSVidPlaybackget_CanStep, get_CanStep, get_CanStep method [Microsoft TV Technologies], get_CanStep method [Microsoft TV Technologies],IMSVidPlayback interface, mstv.imsvidplayback_get_canstep, segment/IMSVidPlayback::get_CanStep
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SourceSizeList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	segment.h
api_name:
-	IMSVidPlayback.get_CanStep
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidPlayback::get_CanStep


## -description


The <b>get_CanStep</b> method queries whether the input source can step frame by frame.


## -parameters




### -param fBackwards [in]

Use one of the following values.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>Query whether the input can step forward</td>
</tr>
<tr>
<td>VARIANT_TRUE</td>
<td>Query whether the input can step backward.</td>
</tr>
</table>
 


### -param pfCan [out]

Pointer to a variable that receives one of the following values.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>The source cannot step in the specified direction.</td>
</tr>
<tr>
<td>VARIANT_TRUE</td>
<td>The source can step in the specified direction.</td>
</tr>
</table>
 


## -returns



The method returns an <b>HRESULT</b>. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The graph is not built. Call the <a href="https://msdn.microsoft.com/49f78dd8-f26e-456d-b67e-155ae0ed5419">Build</a> or <a href="https://msdn.microsoft.com/library/windows/hardware/dn927297">View</a> method on the Video Control.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  The value ERROR_INVALID_STATE is converted to an <b>HRESULT</b> with the <b>HRESULT_FROM_WIN32</b> macro.</div>
<div> </div>



## -remarks



Call the <a href="https://msdn.microsoft.com/49f78dd8-f26e-456d-b67e-155ae0ed5419">IMSVidCtl::Build</a> or <a href="https://msdn.microsoft.com/ec0e2a88-13c0-42f3-ba7d-8ebff1234b86">IMSVidCtl::View</a> method before calling this method.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
VARIANT_BOOL fCan = VARIANT_FALSE;
hr = m_pPlayback-&gt;get_CanStep(VARIANT_FALSE, &amp;fCan);
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ed954545-f58f-4841-9ffd-185350f76388">IMSVidPlayback Interface</a>
 

 

