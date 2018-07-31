---
UID: NF:wmp.IWMPLibrarySharingServices.isLibrarySharingEnabled
title: IWMPLibrarySharingServices::isLibrarySharingEnabled
author: windows-sdk-content
description: The isLibrarySharingEnabled method retrieves a value indicating whether the user has enabled library sharing in Windows Media Player.
old-location: wmp\iwmplibrarysharingservices_islibrarysharingenabled.htm
old-project: WMP
ms.assetid: bd643869-9111-423e-9f9c-7147d1e3c7b8
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWMPLibrarySharingServices interface [Windows Media Player],isLibrarySharingEnabled method, IWMPLibrarySharingServices.isLibrarySharingEnabled, IWMPLibrarySharingServices::isLibrarySharingEnabled, IWMPLibrarySharingServicesisLibrarySharingEnabled, isLibrarySharingEnabled, isLibrarySharingEnabled method [Windows Media Player], isLibrarySharingEnabled method [Windows Media Player],IWMPLibrarySharingServices interface, wmp.iwmplibrarysharingservices_islibrarysharingenabled, wmp/IWMPLibrarySharingServices::isLibrarySharingEnabled
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
 - IWMPLibrarySharingServices.isLibrarySharingEnabled
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPLibrarySharingServices::isLibrarySharingEnabled


## -description



The <b>isLibrarySharingEnabled</b> method retrieves a value indicating whether the user has enabled library sharing in Windows Media Player.




## -parameters




### -param pvbEnabled [out]

Pointer to a <b>VARIANT_BOOL</b> that receives the result. <b>VARIANT_TRUE</b> indicates that the user has enabled library sharing.


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



<b>Windows Media Player 10 Mobile:</b> This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/24cac18c-a3aa-4cd0-b5f7-025db2eed0b8">IWMPLibrarySharingServices Interface</a>
 

 

