---
UID: NF:dsadmin.IDsAdminNotifyHandler.Notify
title: IDsAdminNotifyHandler::Notify (dsadmin.h)
description: Called for each object after the confirmation dialog box has been displayed and the notification handler is selected in the confirmation dialog box.
helpviewer_keywords: ["IDsAdminNotifyHandler interface [Active Directory]","Notify method","IDsAdminNotifyHandler.Notify","IDsAdminNotifyHandler::Notify","Notify","Notify method [Active Directory]","Notify method [Active Directory]","IDsAdminNotifyHandler interface","_glines_idsadminnotifyhandler_notify","ad.idsadminnotifyhandler__notify","ad.idsadminnotifyhandler_notify","dsadmin/IDsAdminNotifyHandler::Notify"]
old-location: ad\idsadminnotifyhandler_notify.htm
tech.root: ad
ms.assetid: ac0b9da5-b0e3-4280-ae9c-602e28c907b1
ms.date: 12/05/2018
ms.keywords: IDsAdminNotifyHandler interface [Active Directory],Notify method, IDsAdminNotifyHandler.Notify, IDsAdminNotifyHandler::Notify, Notify, Notify method [Active Directory], Notify method [Active Directory],IDsAdminNotifyHandler interface, _glines_idsadminnotifyhandler_notify, ad.idsadminnotifyhandler__notify, ad.idsadminnotifyhandler_notify, dsadmin/IDsAdminNotifyHandler::Notify
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDsAdminNotifyHandler::Notify
 - dsadmin/IDsAdminNotifyHandler::Notify
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DSAdmin.dll
api_name:
 - IDsAdminNotifyHandler.Notify
---

# IDsAdminNotifyHandler::Notify


## -description

The <b>IDsAdminNotifyHandler::Notify</b> method is called  for each object after the confirmation dialog box has been displayed and the notification handler is selected in the confirmation dialog box.

## -parameters

### -param nItem [in]

Contains the index of the item in the <b>aObjects</b> member of the <a href="/windows/desktop/api/dsclient/ns-dsclient-dsobjectnames">DSOBJECTNAMES</a> structure supplied in the <a href="/windows/desktop/api/dsadmin/nf-dsadmin-idsadminnotifyhandler-begin">IDsAdminNotifyHandler::Begin</a> method.

### -param uFlags [in]

Contains the flags supplied by the notification handler in the <a href="/windows/desktop/api/dsadmin/nf-dsadmin-idsadminnotifyhandler-begin">IDsAdminNotifyHandler::Begin</a> method.

## -returns

The return value from this method is ignored.

## -see-also

<a href="/windows/desktop/api/dsclient/ns-dsclient-dsobjectnames">DSOBJECTNAMES</a>



<a href="/windows/desktop/api/dsadmin/nn-dsadmin-idsadminnotifyhandler">IDsAdminNotifyHandler</a>



<a href="/windows/desktop/api/dsadmin/nf-dsadmin-idsadminnotifyhandler-begin">IDsAdminNotifyHandler::Begin</a>