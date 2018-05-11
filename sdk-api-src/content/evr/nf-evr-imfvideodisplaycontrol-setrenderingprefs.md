---
UID: NF:evr.IMFVideoDisplayControl.SetRenderingPrefs
title: IMFVideoDisplayControl::SetRenderingPrefs
author: windows-driver-content
description: Sets various preferences related to video rendering.
old-location: mf\imfvideodisplaycontrol_setrenderingprefs.htm
old-project: medfound
ms.assetid: 7603aaf8-1671-4b35-bee5-335f656de3c5
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: 7603aaf8-1671-4b35-bee5-335f656de3c5, IMFVideoDisplayControl interface [Media Foundation],SetRenderingPrefs method, IMFVideoDisplayControl.SetRenderingPrefs, IMFVideoDisplayControl::SetRenderingPrefs, SetRenderingPrefs, SetRenderingPrefs method [Media Foundation], SetRenderingPrefs method [Media Foundation],IMFVideoDisplayControl interface, evr/IMFVideoDisplayControl::SetRenderingPrefs, mf.imfvideodisplaycontrol_setrenderingprefs
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MFVideoMixPrefs
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	strmiids.lib
-	strmiids.dll
api_name:
-	IMFVideoDisplayControl.SetRenderingPrefs
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IMFVideoDisplayControl::SetRenderingPrefs


## -description



Sets various preferences related to video rendering.




## -parameters




### -param dwRenderFlags [in]

Bitwise <b>OR</b> of zero or more flags from the <a href="https://msdn.microsoft.com/a56e7e09-23af-4ad3-9846-4102233ed3c4">MFVideoRenderPrefs</a> enumeration.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid flags.

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
 

 

