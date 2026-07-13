---
UID: NE:devquerydef._DEV_QUERY_FLAGS
tech.root: devinst
title: DEV_QUERY_FLAGS
ms.date: 11/05/2024
targetos: Windows
description: Specifies flags that alter device query behavior.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: devquerydef.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
typedef_isUnnamed: false
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - devquerydef.h
api_name:
 - _DEV_QUERY_FLAGS
 - PDEV_QUERY_FLAGS
 - DEV_QUERY_FLAGS
f1_keywords:
 - _DEV_QUERY_FLAGS
 - devquerydef/_DEV_QUERY_FLAGS
 - PDEV_QUERY_FLAGS
 - devquerydef/PDEV_QUERY_FLAGS
 - DEV_QUERY_FLAGS
 - devquerydef/DEV_QUERY_FLAGS
dev_langs:
 - c++
helpviewer_keywords:
 - _DEV_QUERY_FLAGS
---

## -description

Specifies flags that alter device query behavior.

## -enum-fields

### -field DevQueryFlagNone

No flags specified.

### -field DevQueryFlagUpdateResults

By default, queries do not receive updates. However, when a query registers for updates and specifies the **DevQueryFlagUpdateResults** flag, its result-set will continue to be updated by callbacks as changes in the system occurs that add or remove objects or change objects so that they now match, or no longer match the filter expression.

### -field DevQueryFlagAllProperties

Return all properties in all languages that exist for the object. See **DevQueryFlagLocalize** because it can modify this behavior.

### -field DevQueryFlagLocalize

When specified, properties of type [DEVPROP_TYPE_STRING_INDIRECT](/windows-hardware/drivers/install/devprop-type-string-indirect) are resolved to the calling thread's UI language. Multi-language properties are retrieved in the preferred language of the calling application.

If used in conjunction with **DevQueryFlagAllProperties**, values for all property keys for the object will be fetched in the preferred language of the calling application.

### -field DevQueryFlagAsyncClose

This flag modifies the behavior of the [DevCloseObjectQuery](../devquery/nf-devquery-devcloseobjectquery.md) function. When it is specified,
**DevCloseObjectQuery** will return immediately, but the callback function will continue to be invoked until a [DevQueryStateClosed](ne-devquerydef-dev_query_state.md) state change is received.

When **DevQueryFlagAsyncClose** is not specified, **DevCloseObjectQuery** will block until an outstanding callback returns, and no further callbacks will occur once the **DevCloseObjectQuery** returns.

In either case, a reference is held on the DLL where the callback function is implemented to ensure that it won't be unloaded while callbacks can still be invoked.

## -remarks

## -see-also

