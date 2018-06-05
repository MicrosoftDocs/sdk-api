---
UID: NF:wmp.IWMPCdromRip.get_ripProgress
title: IWMPCdromRip::get_ripProgress
author: windows-sdk-content
description: The get_ripProgress method retrieves the CD ripping progress as percent complete.
old-location: wmp\iwmpcdromrip_get_ripprogress.htm
old-project: WMP
ms.assetid: d7140bc9-bf79-48f0-aaf0-155660c8b2c9
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IWMPCdromRip interface [Windows Media Player],get_ripProgress method, IWMPCdromRip.get_ripProgress, IWMPCdromRip::get_ripProgress, IWMPCdromRipget_ripProgress, get_ripProgress, get_ripProgress method [Windows Media Player], get_ripProgress method [Windows Media Player],IWMPCdromRip interface, wmp.iwmpcdromrip_get_ripprogress, wmp/IWMPCdromRip::get_ripProgress
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11.
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
tech.root: 
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.dll
api_name:
-	IWMPCdromRip.get_ripProgress
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPCdromRip::get_ripProgress


## -description



The <b>get_ripProgress</b> method retrieves the CD ripping progress as percent complete.




## -parameters




### -param plProgress [out]

Pointer to a <b>long</b> that receives the progress value. Progress values range from 0 to 100.


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
</table>
 




## -remarks



The progress value represents the completed percentage of the entire ripping process. To determine the progress of a specific track, use <a href="https://msdn.microsoft.com/ee964f68-d44c-4e66-908b-09070a96d96f">IWMPMedia::getItemInfo</a> with <b>RipProgress</b> as the attribute name. To determine the index of the track currently being ripped, call <a href="https://msdn.microsoft.com/c6763274-01e4-4a2f-9467-150e1964193a">IWMPPlaylist::getItemInfo</a> with <b>CurrentRipTrackIndex</b> as the attribute name.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/c3e2db46-bef0-4c79-91b5-97ca5a86c6ba">IWMPCdromRip Interface</a>



<a href="https://msdn.microsoft.com/f5c1b5bf-d616-48cb-8690-e0237c56e402">Ripping a CD</a>
 

 

