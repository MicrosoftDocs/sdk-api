---
UID: NF:wmp.IWMPPlayerApplication.switchToPlayerApplication
title: IWMPPlayerApplication::switchToPlayerApplication
author: windows-sdk-content
description: The switchToPlayerApplication method switches a remoted Windows Media Player control to the full mode of the Player.
old-location: wmp\iwmpplayerapplication_switchtoplayerapplication.htm
old-project: WMP
ms.assetid: cf5a77c5-298e-48de-80cd-d7ecd9e74323
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMPPlayerApplication interface [Windows Media Player],switchToPlayerApplication method, IWMPPlayerApplication.switchToPlayerApplication, IWMPPlayerApplication::switchToPlayerApplication, IWMPPlayerApplicationswitchToPlayerApplication, switchToPlayerApplication, switchToPlayerApplication method [Windows Media Player], switchToPlayerApplication method [Windows Media Player],IWMPPlayerApplication interface, wmp.iwmpplayerapplication_switchtoplayerapplication, wmp/IWMPPlayerApplication::switchToPlayerApplication
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
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
 - IWMPPlayerApplication.switchToPlayerApplication
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPPlayerApplication::switchToPlayerApplication


## -description



The <b>switchToPlayerApplication</b> method switches a remoted Windows Media Player control to the full mode of the Player.




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



This method is used only when remoting the Windows Media Player control.

<b>Windows Media Player 10 Mobile: </b>This method always returns E_NOTIMPL.




## -see-also




<a href="https://msdn.microsoft.com/bcdd7ea9-66b2-40e9-89a1-0fec073ccd92">IWMPPlayerApplication Interface</a>



<a href="https://msdn.microsoft.com/d543b2a0-a2cb-47e2-b50e-4513fc061b46">Remoting the Windows Media Player Control</a>
 

 

