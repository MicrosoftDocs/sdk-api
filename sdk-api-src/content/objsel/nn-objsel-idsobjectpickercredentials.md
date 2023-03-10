---
UID: NN:objsel.IDsObjectPickerCredentials
title: IDsObjectPickerCredentials (objsel.h)
description: The IDsObjectPickerCredentials interface allows you to override credentials for the IDsObjectPicker object implementing this interface.
helpviewer_keywords: ["IDsObjectPickerCredentials","IDsObjectPickerCredentials object [Active Directory]","IDsObjectPickerCredentials object [Active Directory]","described","ad.idsobjectpickercredentials","objsel/IDsObjectPickerCredentials"]
old-location: ad\idsobjectpickercredentials.htm
tech.root: ad
ms.assetid: 336e7e68-0903-42f7-9810-53ccceed32de
ms.date: 12/05/2018
ms.keywords: IDsObjectPickerCredentials, IDsObjectPickerCredentials object [Active Directory], IDsObjectPickerCredentials object [Active Directory],described, ad.idsobjectpickercredentials, objsel/IDsObjectPickerCredentials
req.header: objsel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.dll: Objsel.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDsObjectPickerCredentials
 - objsel/IDsObjectPickerCredentials
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Objsel.dll
api_name:
 - IDsObjectPickerCredentials
---

# IDsObjectPickerCredentials interface


## -description

The <b>IDsObjectPickerCredentials</b> interface 
    allows you to override credentials for the <a href="/windows/desktop/api/objsel/nn-objsel-idsobjectpicker">IDsObjectPicker</a> 
    object implementing this interface.

To obtain an instance of this interface, call 
    <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> with the 
    <b>IID_IDsObjectPickerCredentials</b> interface identifier as shown below.

