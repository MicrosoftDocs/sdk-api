---
UID: NF:dsadmin.IDsAdminNotifyHandler.Notify
title: IDsAdminNotifyHandler::Notify
author: windows-sdk-content
description: Called for each object after the confirmation dialog box has been displayed and the notification handler is selected in the confirmation dialog box.
old-location: ad\idsadminnotifyhandler_notify.htm
tech.root: ad
ms.assetid: ac0b9da5-b0e3-4280-ae9c-602e28c907b1
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IDsAdminNotifyHandler interface [Active Directory],Notify method, IDsAdminNotifyHandler.Notify, IDsAdminNotifyHandler::Notify, Notify, Notify method [Active Directory], Notify method [Active Directory],IDsAdminNotifyHandler interface, _glines_idsadminnotifyhandler_notify, ad.idsadminnotifyhandler__notify, ad.idsadminnotifyhandler_notify, dsadmin/IDsAdminNotifyHandler::Notify
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dsadmin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: DSAdmin.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DSAdmin.dll
api_name:
 - IDsAdminNotifyHandler.Notify
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDsAdminNotifyHandler::Notify


## -description


The <b>IDsAdminNotifyHandler::Notify</b> method is called  for each object after the confirmation dialog box has been displayed and the notification handler is selected in the confirmation dialog box.


## -parameters




### -param nItem [in]

Contains the index of the item in the <b>aObjects</b> member of the <a href="https://msdn.microsoft.com/dfc1e88f-40ff-4ec1-9718-4801f678fa3f">DSOBJECTNAMES</a> structure supplied in the <a href="https://msdn.microsoft.com/443fe344-6545-45bd-8e2f-85347505d407">IDsAdminNotifyHandler::Begin</a> method.


### -param uFlags [in]

Contains the flags supplied by the notification handler in the <a href="https://msdn.microsoft.com/443fe344-6545-45bd-8e2f-85347505d407">IDsAdminNotifyHandler::Begin</a> method.


## -returns



The return value from this method is ignored.




## -see-also




<a href="https://msdn.microsoft.com/dfc1e88f-40ff-4ec1-9718-4801f678fa3f">DSOBJECTNAMES</a>



<a href="https://msdn.microsoft.com/d55e1473-8e51-441e-bd22-63208b294e14">IDsAdminNotifyHandler</a>



<a href="https://msdn.microsoft.com/443fe344-6545-45bd-8e2f-85347505d407">IDsAdminNotifyHandler::Begin</a>
 

 

