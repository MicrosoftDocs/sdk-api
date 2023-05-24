---
UID: NF:cfapi.CfGetPlaceholderStateFromAttributeTag
title: CfGetPlaceholderStateFromAttributeTag function (cfapi.h)
description: Gets a set of placeholder states based on the FileAttributes and ReparseTag values of the file.
helpviewer_keywords: ["CfGetPlaceholderStateFromAttributeTag","CfGetPlaceholderStateFromAttributeTag function","cfapi/CfGetPlaceholderStateFromAttributeTag","cloudApi.cfgetplaceholderstatefromattributetag"]
old-location: cloudapi\cfgetplaceholderstatefromattributetag.htm
tech.root: cloudapi
ms.assetid: D7B4FB60-3388-489F-9F55-153B53BBDA9F
ms.date: 12/05/2018
ms.keywords: CfGetPlaceholderStateFromAttributeTag, CfGetPlaceholderStateFromAttributeTag function, cfapi/CfGetPlaceholderStateFromAttributeTag, cloudApi.cfgetplaceholderstatefromattributetag
req.header: cfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: CldApi.lib
req.dll: CldApi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CfGetPlaceholderStateFromAttributeTag
 - cfapi/CfGetPlaceholderStateFromAttributeTag
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CldApi.dll
api_name:
 - CfGetPlaceholderStateFromAttributeTag
---

# CfGetPlaceholderStateFromAttributeTag function

## -description

Gets a set of placeholder states based on the *FileAttributes* and *ReparseTag* values of the file.

## -parameters

### -param FileAttributes [in]

The file attribute information.

### -param ReparseTag [in]

The reparse tag information from a file.

## -returns

Can include [CF_PLACEHOLDER_STATE](ne-cfapi-cf_placeholder_state.md); the placeholder state.

## -remarks

The *FileAttributes* and *ReparseTag* can be obtained by listing the directory containing the file or by directly querying *FileAttributeTagInfo* on the file.

The following [CF_PLACEHOLDER_STATE](ne-cfapi-cf_placeholder_state.md) values can be returned:

| Placeholder state | Description |
| **CF_PLACEHOLDER_STATE_NO_STATES** | When returned, the file or directory whose attributes and reparse tag examined by the API is not a cloud files placeholder. |
| **CF_PLACEHOLDER_STATE_PLACEHOLDER** | When set, the file or directory whose attributes and reparse tag examined by the API is a cloud files placeholder. |
| **CF_PLACEHOLDER_STATE_SYNC_ROOT** | When set, the directory is not only a cloud files placeholder directory but also the sync root. |
| **CF_PLACEHOLDER_STATE_ESSENTIAL_PROP_PRESENT** | When set, the file or directory must be a cloud files placeholder, and there exists an essential property in the property store of the file or directory. |
| **CF_PLACEHOLDER_STATE_IN_SYNC** | When set, the file or directory must be a cloud files placeholder, and its content is in sync with the cloud. |
| **CF_PLACEHOLDER_STATE_PARTIAL** | When set, the file or directory must be a cloud files placeholder, and its content is not ready to be consumed by the user application (though it may or may not be fully present locally). An example is a placeholder file whose content has been fully downloaded to the local disk but yet to be validated by a sync provider that has registered the sync root with the hydration modifier **VERIFICATION_REQUIRED**. |
| **CF_PLACEHOLDER_STATE_PARTIALLY_ON_DISK** | When set, the file or directory must be a cloud files placeholder and its content is not fully present locally. When **PARTIALLY_ON_DISK** is set, **PARTIAL** must also be set. |
| **CF_PLACEHOLDER_STATE_INVALID** | This is an invalid state when the API fails to parse the various information of the file or directory. |

## -see-also

[CF_PLACEHOLDER_STATE](ne-cfapi-cf_placeholder_state.md)
