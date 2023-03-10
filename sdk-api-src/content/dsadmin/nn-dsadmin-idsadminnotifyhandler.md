---
UID: NN:dsadmin.IDsAdminNotifyHandler
title: IDsAdminNotifyHandler (dsadmin.h)
description: The IDsAdminNotifyHandler interface is implemented by an Active Directory administrative notification handler.
helpviewer_keywords: ["IDsAdminNotifyHandler","IDsAdminNotifyHandler interface [Active Directory]","IDsAdminNotifyHandler interface [Active Directory]","described","_glines_idsadminnotifyhandler","ad.idsadminnotifyhandler","dsadmin/IDsAdminNotifyHandler"]
old-location: ad\idsadminnotifyhandler.htm
tech.root: ad
ms.assetid: d55e1473-8e51-441e-bd22-63208b294e14
ms.date: 12/05/2018
ms.keywords: IDsAdminNotifyHandler, IDsAdminNotifyHandler interface [Active Directory], IDsAdminNotifyHandler interface [Active Directory],described, _glines_idsadminnotifyhandler, ad.idsadminnotifyhandler, dsadmin/IDsAdminNotifyHandler
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
 - IDsAdminNotifyHandler
 - dsadmin/IDsAdminNotifyHandler
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
 - IDsAdminNotifyHandler
---

# IDsAdminNotifyHandler interface


## -description

The <b>IDsAdminNotifyHandler</b> interface is implemented by an Active Directory administrative notification handler. This interface is used by the Active Directory Users and Computers MMC snap-in to notify registered handlers when certain events, such as deleting or renaming an object, occur. The snap-in creates an instance of this object by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> with the CLSID of the extension.

## -inheritance

The <b>IDsAdminNotifyHandler</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDsAdminNotifyHandler</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>
