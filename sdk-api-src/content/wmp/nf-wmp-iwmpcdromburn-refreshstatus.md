---
UID: NF:wmp.IWMPCdromBurn.refreshStatus
title: IWMPCdromBurn::refreshStatus
author: windows-sdk-content
description: The refreshStatus method updates the status information for the current burn playlist.
old-location: wmp\iwmpcdromburn_refreshstatus.htm
tech.root: WMP
ms.assetid: 7a1ca071-0a61-4ef5-b8c1-18336cf5b1b0
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWMPCdromBurn interface [Windows Media Player],refreshStatus method, IWMPCdromBurn.refreshStatus, IWMPCdromBurn::refreshStatus, IWMPCdromBurnrefreshStatus, refreshStatus, refreshStatus method [Windows Media Player], refreshStatus method [Windows Media Player],IWMPCdromBurn interface, wmp.iwmpcdromburn_refreshstatus, wmp/IWMPCdromBurn::refreshStatus
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: Wmp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPCdromBurn.refreshStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wmp.h
: 
- IWMPCdromBurn.refreshStatus
: 
---

# IWMPCdromBurn::refreshStatus


## -description



The <b>refreshStatus</b> method updates the status information for the current burn playlist.




## -parameters






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



You should call this method after you create or change a burn playlist before reading status information or burning the CD. You can test whether a refresh is required by calling <b>get_burnState</b> and checking for wmpbsRefreshStatusPending.

Refreshing the status is a synchronous operation. This means that a lengthy period of time might elapse before this method returns if the current burn playlist is large and contains many changes.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/45116a33-62f9-4c7d-b246-25905cbaf118">IWMPCdromBurn Interface</a>



<a href="https://msdn.microsoft.com/a6bcb8d6-07ad-4d8f-a94a-6b8c1b7f0c2b">IWMPCdromBurn::get_burnState</a>



<a href="https://msdn.microsoft.com/fd286f68-4d36-48ae-800e-ad2be4c613c1">WMPBurnState</a>
 

 

