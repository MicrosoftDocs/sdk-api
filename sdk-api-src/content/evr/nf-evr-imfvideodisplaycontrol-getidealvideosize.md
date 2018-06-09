---
UID: NF:evr.IMFVideoDisplayControl.GetIdealVideoSize
title: IMFVideoDisplayControl::GetIdealVideoSize
author: windows-sdk-content
description: Gets the range of sizes that the enhanced video renderer (EVR) can display without significantly degrading performance or image quality.
old-location: mf\imfvideodisplaycontrol_getidealvideosize.htm
old-project: medfound
ms.assetid: c580778b-fe7c-4c62-9bcd-8a5fde370b9d
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: GetIdealVideoSize, GetIdealVideoSize method [Media Foundation], GetIdealVideoSize method [Media Foundation],IMFVideoDisplayControl interface, IMFVideoDisplayControl interface [Media Foundation],GetIdealVideoSize method, IMFVideoDisplayControl.GetIdealVideoSize, IMFVideoDisplayControl::GetIdealVideoSize, c580778b-fe7c-4c62-9bcd-8a5fde370b9d, evr/IMFVideoDisplayControl::GetIdealVideoSize, mf.imfvideodisplaycontrol_getidealvideosize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: evr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MFVideoMixPrefs
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFVideoDisplayControl.GetIdealVideoSize
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IMFVideoDisplayControl::GetIdealVideoSize


## -description



          Gets the range of sizes that the enhanced video renderer (EVR) can display without significantly degrading performance or image quality.
        


## -parameters




### -param pszMin [in, out]

Receives the minimum ideal size. This parameter can be <b>NULL</b>.


### -param pszMax [in, out]

Receives the maximum ideal size. This parameter can be <b>NULL</b>.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
At least one parameter must be non-<b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The video renderer has been shut down.

</td>
</tr>
</table>
 




## -remarks



You can set <i>pszMin</i> or <i>pszMax</i> to <b>NULL</b>, but not both.




## -see-also




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/db9b4663-9240-484f-8c47-cb1f5daa238d">IMFVideoDisplayControl</a>



<a href="https://msdn.microsoft.com/09501d67-effb-41ce-a7b7-d2415acdf3ac">Using the Video Display Controls</a>
 

 

