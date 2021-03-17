---
UID: NF:objsel.IDsObjectPicker.Initialize
title: IDsObjectPicker::Initialize (objsel.h)
description: The IDsObjectPicker::Initialize method initializes the object picker dialog box with data about the scopes, filters, and options used by the object picker dialog box.
helpviewer_keywords: ["IDsObjectPicker interface [Active Directory]","Initialize method","IDsObjectPicker.Initialize","IDsObjectPicker::Initialize","Initialize","Initialize method [Active Directory]","Initialize method [Active Directory]","IDsObjectPicker interface","_glines_idsobjectpicker_initialize","ad.idsobjectpicker__initialize","ad.idsobjectpicker_initialize","objsel/IDsObjectPicker::Initialize"]
old-location: ad\idsobjectpicker_initialize.htm
tech.root: ad
ms.assetid: bcf4d283-6709-4425-a122-8f0808502b58
ms.date: 12/05/2018
ms.keywords: IDsObjectPicker interface [Active Directory],Initialize method, IDsObjectPicker.Initialize, IDsObjectPicker::Initialize, Initialize, Initialize method [Active Directory], Initialize method [Active Directory],IDsObjectPicker interface, _glines_idsobjectpicker_initialize, ad.idsobjectpicker__initialize, ad.idsobjectpicker_initialize, objsel/IDsObjectPicker::Initialize
req.header: objsel.h
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
req.dll: Objsel.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDsObjectPicker::Initialize
 - objsel/IDsObjectPicker::Initialize
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
 - IDsObjectPicker.Initialize
---

# IDsObjectPicker::Initialize


## -description

The <b>IDsObjectPicker::Initialize</b> method initializes the object picker dialog box with data about the scopes, filters, and options used by the object picker dialog box.

## -parameters

### -param pInitInfo

Pointer to a 
<a href="/windows/desktop/api/objsel/ns-objsel-dsop_init_info">DSOP_INIT_INFO</a> structure that contains the initialization data.

## -returns

Returns a standard error code or one of the following values.

## -remarks

<b>IDsObjectPicker::Initialize</b> can be called more than once and the last call takes precedence. The <a href="/windows/desktop/api/objsel/nn-objsel-idsobjectpicker">IDsObjectPicker</a> object will completely re-initialize itself in response  to this method.

## -see-also

<a href="/windows/desktop/api/objsel/ns-objsel-dsop_init_info">DSOP_INIT_INFO</a>



<a href="/windows/desktop/AD/directory-object-picker">Directory Object Picker</a>



<a href="/windows/desktop/api/objsel/nn-objsel-idsobjectpicker">IDsObjectPicker</a>