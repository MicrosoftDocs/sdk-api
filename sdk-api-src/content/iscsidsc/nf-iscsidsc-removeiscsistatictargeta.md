---
UID: NF:iscsidsc.RemoveIScsiStaticTargetA
title: RemoveIScsiStaticTargetA function (iscsidsc.h)
description: RemoveIscsiStaticTarget function removes a target from the list of static targets made available to the machine. (ANSI)
helpviewer_keywords: ["RemoveIScsiStaticTargetA", "RemoveIscsiStaticTargetA", "iscsidsc/RemoveIscsiStaticTargetA"]
old-location: iscsidisc\removeiscsistatictarget.htm
tech.root: iSCSIDisc
ms.assetid: 7927d414-929e-4f01-b6bf-e6d571486aed
ms.date: 12/05/2018
ms.keywords: RemoveIScsiStaticTargetA, RemoveIscsiStaticTarget, RemoveIscsiStaticTarget function [iSCSI Discovery Library API], RemoveIscsiStaticTargetA, RemoveIscsiStaticTargetW, iscsidisc.removeiscsistatictarget, iscsidsc/RemoveIscsiStaticTarget, iscsidsc/RemoveIscsiStaticTargetA, iscsidsc/RemoveIscsiStaticTargetW
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RemoveIscsiStaticTargetW (Unicode) and RemoveIscsiStaticTargetA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Iscsidsc.lib
req.dll: Iscsidsc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RemoveIScsiStaticTargetA
 - iscsidsc/RemoveIScsiStaticTargetA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iscsidsc.dll
api_name:
 - RemoveIscsiStaticTarget
 - RemoveIscsiStaticTargetA
 - RemoveIscsiStaticTargetW
---

# RemoveIScsiStaticTargetA function


## -description

The <b>RemoveIscsiStaticTarget</b> function removes a target from the list of static targets made available to the machine.

## -parameters

### -param TargetName [in]

The name of the iSCSI target to remove from the static list.

## -returns

Returns ERROR_SUCCESS if the operation succeeds. Otherwise, it returns the appropriate Win32 or iSCSI error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-addiscsistatictargeta">AddIscsiStaticTarget</a>

## -remarks

> [!NOTE]
> The iscsidsc.h header defines RemoveIScsiStaticTarget as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
