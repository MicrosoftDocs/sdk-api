---
UID: NF:evr.IMFVideoDisplayControl.GetRenderingPrefs
title: IMFVideoDisplayControl::GetRenderingPrefs
author: windows-sdk-content
description: Gets various video rendering settings.
old-location: mf\imfvideodisplaycontrol_getrenderingprefs.htm
old-project: medfound
ms.assetid: 9a5bd1d6-e604-4798-af29-ad0c1931b651
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: 9a5bd1d6-e604-4798-af29-ad0c1931b651, GetRenderingPrefs, GetRenderingPrefs method [Media Foundation], GetRenderingPrefs method [Media Foundation],IMFVideoDisplayControl interface, IMFVideoDisplayControl interface [Media Foundation],GetRenderingPrefs method, IMFVideoDisplayControl.GetRenderingPrefs, IMFVideoDisplayControl::GetRenderingPrefs, evr/IMFVideoDisplayControl::GetRenderingPrefs, mf.imfvideodisplaycontrol_getrenderingprefs
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
 - IMFVideoDisplayControl.GetRenderingPrefs
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IMFVideoDisplayControl::GetRenderingPrefs


## -description


Gets various video rendering settings.
        


## -parameters




### -param pdwRenderFlags [out]

Receives a bitwise <b>OR</b> of zero or more flags from the <a href="https://msdn.microsoft.com/a56e7e09-23af-4ad3-9846-4102233ed3c4">MFVideoRenderPrefs</a> enumeration.


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
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The video renderer has been shut down.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/db9b4663-9240-484f-8c47-cb1f5daa238d">IMFVideoDisplayControl</a>



<a href="https://msdn.microsoft.com/09501d67-effb-41ce-a7b7-d2415acdf3ac">Using the Video Display Controls</a>
 

 

