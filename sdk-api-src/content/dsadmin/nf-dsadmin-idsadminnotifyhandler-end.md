---
UID: NF:dsadmin.IDsAdminNotifyHandler.End
title: IDsAdminNotifyHandler::End (dsadmin.h)
description: The IDsAdminNotifyHandler::End method is called after the notification event has occurred. This method is called even if the notification process is canceled.
helpviewer_keywords: ["End","End method [Active Directory]","End method [Active Directory]","IDsAdminNotifyHandler interface","IDsAdminNotifyHandler interface [Active Directory]","End method","IDsAdminNotifyHandler.End","IDsAdminNotifyHandler::End","_glines_idsadminnotifyhandler_end","ad.idsadminnotifyhandler__end","ad.idsadminnotifyhandler_end","dsadmin/IDsAdminNotifyHandler::End"]
old-location: ad\idsadminnotifyhandler_end.htm
tech.root: ad
ms.assetid: 6ff92b54-fa2c-4f45-8f40-e9c884e9cf7e
ms.date: 12/05/2018
ms.keywords: End, End method [Active Directory], End method [Active Directory],IDsAdminNotifyHandler interface, IDsAdminNotifyHandler interface [Active Directory],End method, IDsAdminNotifyHandler.End, IDsAdminNotifyHandler::End, _glines_idsadminnotifyhandler_end, ad.idsadminnotifyhandler__end, ad.idsadminnotifyhandler_end, dsadmin/IDsAdminNotifyHandler::End
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
 - IDsAdminNotifyHandler::End
 - dsadmin/IDsAdminNotifyHandler::End
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
 - IDsAdminNotifyHandler.End
---

# IDsAdminNotifyHandler::End


## -description

The <b>IDsAdminNotifyHandler::End</b> method is called after the notification event has occurred. This method is called even if the notification process is canceled.



## -returns

The return value from this method is ignored.

## -remarks

This method provides the opportunity for the notification handler to free any memory allocated during the <a href="/windows/desktop/api/dsadmin/nf-dsadmin-idsadminnotifyhandler-begin">IDsAdminNotifyHandler::Begin</a> or <a href="/windows/desktop/api/dsadmin/nf-dsadmin-idsadminnotifyhandler-notify">IDsAdminNotifyHandler::Notify</a> methods.

## -see-also

<a href="/windows/desktop/api/dsadmin/nn-dsadmin-idsadminnotifyhandler">IDsAdminNotifyHandler</a>



<a href="/windows/desktop/api/dsadmin/nf-dsadmin-idsadminnotifyhandler-begin">IDsAdminNotifyHandler::Begin</a>



<a href="/windows/desktop/api/dsadmin/nf-dsadmin-idsadminnotifyhandler-notify">IDsAdminNotifyHandler::Notify</a>
