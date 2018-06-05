---
UID: NF:segment.IMSVidPlayback.get_Length
title: IMSVidPlayback::get_Length
author: windows-sdk-content
description: The get_Length method retrieves the length of the playback source.
old-location: mstv\imsvidplayback_get_length.htm
old-project: mstv
ms.assetid: a559c0b4-ed63-47ef-b99a-866c87939d5b
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IMSVidPlayback interface [Microsoft TV Technologies],get_Length method, IMSVidPlayback.get_Length, IMSVidPlayback::get_Length, IMSVidPlaybackget_Length, get_Length, get_Length method [Microsoft TV Technologies], get_Length method [Microsoft TV Technologies],IMSVidPlayback interface, mstv.imsvidplayback_get_length, segment/IMSVidPlayback::get_Length
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
tech.root: 
req.typenames: SourceSizeList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	segment.h
api_name:
-	IMSVidPlayback.get_Length
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidPlayback::get_Length


## -description


The <b>get_Length</b> method retrieves the length of the playback source.


## -parameters




### -param lLength [out]

Pointer to a variable that receives the length. The units for the returned value are determined by the current position mode.

<table>
<tr>
<th>
                  Position Mode
                </th>
<th>
                  Returned Value
                </th>
</tr>
<tr>
<td>FrameMode</td>
<td>Frame number</td>
</tr>
<tr>
<td>TenthsSecondsMode</td>
<td>Hundredths of seconds</td>
</tr>
</table>
 

To set the position mode, call <a href="https://msdn.microsoft.com/b2ff0b7e-c35d-4ea9-92de-a31654781687">IMSVidPlayback::put_PositionMode</a>.


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
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The source does not support getting the length.

</td>
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




## -see-also




<a href="https://msdn.microsoft.com/ed954545-f58f-4841-9ffd-185350f76388">IMSVidPlayback Interface</a>
 

 

