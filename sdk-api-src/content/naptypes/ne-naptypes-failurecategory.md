---
UID: NE:naptypes.tagFailureCategory
title: FailureCategory (naptypes.h)
description: Indicates the source of a failure.
helpviewer_keywords: ["FailureCategory","FailureCategory enumeration [NAP]","failureCategoryClientCommunication","failureCategoryClientComponent","failureCategoryNone","failureCategoryOther","failureCategoryServerCommunication","failureCategoryServerComponent","nap.failurecategory_enum","naptypes/FailureCategory","naptypes/failureCategoryClientCommunication","naptypes/failureCategoryClientComponent","naptypes/failureCategoryNone","naptypes/failureCategoryOther","naptypes/failureCategoryServerCommunication","naptypes/failureCategoryServerComponent"]
old-location: nap\failurecategory_enum.htm
tech.root: NAP
ms.assetid: 3f528702-c9f3-4a91-960b-8b3f3eea91e9
ms.date: 12/05/2018
ms.keywords: FailureCategory, FailureCategory enumeration [NAP], failureCategoryClientCommunication, failureCategoryClientComponent, failureCategoryNone, failureCategoryOther, failureCategoryServerCommunication, failureCategoryServerComponent, nap.failurecategory_enum, naptypes/FailureCategory, naptypes/failureCategoryClientCommunication, naptypes/failureCategoryClientComponent, naptypes/failureCategoryNone, naptypes/failureCategoryOther, naptypes/failureCategoryServerCommunication, naptypes/failureCategoryServerComponent
req.header: naptypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: NapTypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FailureCategory
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagFailureCategory
 - naptypes/tagFailureCategory
 - FailureCategory
 - naptypes/FailureCategory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - NapTypes.h
api_name:
 - FailureCategory
---

# FailureCategory enumeration


## -description

<div class="alert"><b>Note</b>  The Network Access Protection platform is not available starting with Windows 10</div><div> </div>The <b>FailureCategory</b> enumeration indicates the source of a failure.

## -enum-fields

### -field failureCategoryNone:0

No failure.

### -field failureCategoryOther:1

A failure which is not due to client or server components or communications.

### -field failureCategoryClientComponent:2

Failure due to client component.

### -field failureCategoryClientCommunication:3

Failure due to client communication.

### -field failureCategoryServerComponent:4

Failure due to server component.

### -field failureCategoryServerCommunication:5

Failure due to server communication.

## -see-also

<a href="/windows/desktop/api/naptypes/ns-naptypes-failurecategorymapping">FailureCategoryMapping</a>
