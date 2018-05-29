---
UID: NF:wmp.IWMPCdromBurn.erase
title: IWMPCdromBurn::erase
author: windows-sdk-content
description: The erase method erases the current CD.
old-location: wmp\iwmpcdromburn_erase.htm
old-project: WMP
ms.assetid: 93a37f59-4269-4f84-93dc-8350aabd4ebe
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IWMPCdromBurn interface [Windows Media Player],erase method, IWMPCdromBurn.erase, IWMPCdromBurn::erase, IWMPCdromBurnerase, erase, erase method [Windows Media Player], erase method [Windows Media Player],IWMPCdromBurn interface, wmp.iwmpcdromburn_erase, wmp/IWMPCdromBurn::erase
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
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.dll
api_name:
-	IWMPCdromBurn.erase
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPCdromBurn::erase


## -description



The <b>erase</b> method erases the current CD.




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



<b>Windows Media Player 10 Mobile: </b>This method is not supported.

This method will not work if the disc in the drive is not rewritable. Use <a href="https://msdn.microsoft.com/11876b73-10a1-49e2-ad45-33d9641c3647">IWMPCdromBurn::isAvailable</a> to determine whether a CD can be erased.




## -see-also




<a href="https://msdn.microsoft.com/45116a33-62f9-4c7d-b246-25905cbaf118">IWMPCdromBurn Interface</a>
 

 

