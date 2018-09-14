---
UID: NF:dsadmin.IDsAdminNotifyHandler.End
title: IDsAdminNotifyHandler::End
author: windows-sdk-content
description: The IDsAdminNotifyHandler::End method is called after the notification event has occurred. This method is called even if the notification process is canceled.
old-location: ad\idsadminnotifyhandler_end.htm
tech.root: ad
ms.assetid: 6ff92b54-fa2c-4f45-8f40-e9c884e9cf7e
ms.author: windowssdkdev
ms.date: 09/07/2018
ms.keywords: End, End method [Active Directory], End method [Active Directory],IDsAdminNotifyHandler interface, IDsAdminNotifyHandler interface [Active Directory],End method, IDsAdminNotifyHandler.End, IDsAdminNotifyHandler::End, _glines_idsadminnotifyhandler_end, ad.idsadminnotifyhandler__end, ad.idsadminnotifyhandler_end, dsadmin/IDsAdminNotifyHandler::End
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
 - IDsAdminNotifyHandler.End
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDsAdminNotifyHandler::End


## -description


The <b>IDsAdminNotifyHandler::End</b> method is called after the notification event has occurred. This method is called even if the notification process is canceled.


## -parameters






## -returns



The return value from this method is ignored.




## -remarks



This method provides the opportunity for the notification handler to free any memory allocated during the <a href="https://msdn.microsoft.com/443fe344-6545-45bd-8e2f-85347505d407">IDsAdminNotifyHandler::Begin</a> or <a href="https://msdn.microsoft.com/ac0b9da5-b0e3-4280-ae9c-602e28c907b1">IDsAdminNotifyHandler::Notify</a> methods.




## -see-also




<a href="https://msdn.microsoft.com/d55e1473-8e51-441e-bd22-63208b294e14">IDsAdminNotifyHandler</a>



<a href="https://msdn.microsoft.com/443fe344-6545-45bd-8e2f-85347505d407">IDsAdminNotifyHandler::Begin</a>



<a href="https://msdn.microsoft.com/ac0b9da5-b0e3-4280-ae9c-602e28c907b1">IDsAdminNotifyHandler::Notify</a>
 

 

