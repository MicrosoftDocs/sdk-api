---
UID: NF:wmp.IWMPCdromBurn.startBurn
title: IWMPCdromBurn::startBurn
author: windows-sdk-content
description: The startBurn method burns the CD.
old-location: wmp\iwmpcdromburn_startburn.htm
old-project: WMP
ms.assetid: 35357dca-4093-4c83-9cc9-f0dee1241e76
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWMPCdromBurn interface [Windows Media Player],startBurn method, IWMPCdromBurn.startBurn, IWMPCdromBurn::startBurn, IWMPCdromBurnstartBurn, startBurn, startBurn method [Windows Media Player], startBurn method [Windows Media Player],IWMPCdromBurn interface, wmp.iwmpcdromburn_startburn, wmp/IWMPCdromBurn::startBurn
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPCdromBurn.startBurn
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPCdromBurn::startBurn


## -description



The <b>startBurn</b> method burns the CD.




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



The burn state should be wmpbsReady or wmpbsStopped before calling this method.

This method will not work if the CD drive is not a burner, or if the disc in the drive is not writable. Use <a href="https://msdn.microsoft.com/11876b73-10a1-49e2-ad45-33d9641c3647">IWMPCdromBurn::isAvailable</a> to determine whether a CD can be burned.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/45116a33-62f9-4c7d-b246-25905cbaf118">IWMPCdromBurn Interface</a>



<a href="https://msdn.microsoft.com/a6bcb8d6-07ad-4d8f-a94a-6b8c1b7f0c2b">IWMPCdromBurn::get_burnState</a>



<a href="https://msdn.microsoft.com/cf001a08-97e9-4f88-919a-54651e3bfd5d">IWMPCdromBurn::stopBurn</a>
 

 

