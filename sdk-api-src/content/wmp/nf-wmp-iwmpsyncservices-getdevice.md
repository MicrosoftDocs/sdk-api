---
UID: NF:wmp.IWMPSyncServices.getDevice
title: IWMPSyncServices::getDevice
author: windows-sdk-content
description: The getDevice method retrieves a pointer to a device interface.
old-location: wmp\iwmpsyncservices_getdevice.htm
old-project: WMP
ms.assetid: 4c34b823-57ce-4053-9e98-308a5d4ffdef
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMPSyncServices interface [Windows Media Player],getDevice method, IWMPSyncServices.getDevice, IWMPSyncServices::getDevice, IWMPSyncServicesgetDevice, getDevice, getDevice method [Windows Media Player], getDevice method [Windows Media Player],IWMPSyncServices interface, wmp.iwmpsyncservices_getdevice, wmp/IWMPSyncServices::getDevice
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 10 or later.
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
 - IWMPSyncServices.getDevice
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPSyncServices::getDevice


## -description



The <b>getDevice</b> method retrieves a pointer to a device interface.




## -parameters




### -param lIndex [in]

<b>long</b> that contains the index of the device to retrieve. Device indexes are zero-based.


### -param ppDevice [out]

Pointer to a pointer to an <b>IWMPSyncDevice</b> interface that represents the device having the specified index.


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
<dt><b>NS_E_PDA_INITIALIZINGDEVICES (0xC00D118D)</b></dt>
</dl>
</td>
<td width="60%">
Windows Media Player is currently busy initializing devices. Please try again later.

</td>
</tr>
</table>
 




## -remarks



<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/57db3646-2f79-4087-98b2-2bc9d2f3c866">IWMPSyncServices Interface</a>
 

 

