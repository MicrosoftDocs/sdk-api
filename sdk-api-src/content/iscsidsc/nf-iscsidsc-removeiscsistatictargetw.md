---
UID: NF:iscsidsc.RemoveIScsiStaticTargetW
title: RemoveIScsiStaticTargetW function (iscsidsc.h)

description: RemoveIscsiStaticTarget function removes a target from the list of static targets made available to the machine.
old-location: iscsidisc\removeiscsistatictarget.htm
tech.root: iSCSIDisc
ms.assetid: 7927d414-929e-4f01-b6bf-e6d571486aed

ms.date: 12/05/2018
ms.keywords: RemoveIScsiStaticTargetW, RemoveIscsiStaticTarget, RemoveIscsiStaticTarget function [iSCSI Discovery Library API], RemoveIscsiStaticTargetA, RemoveIscsiStaticTargetW, iscsidisc.removeiscsistatictarget, iscsidsc/RemoveIscsiStaticTarget, iscsidsc/RemoveIscsiStaticTargetA, iscsidsc/RemoveIscsiStaticTargetW
ms.topic: function
f1_keywords: 
 - "iscsidsc/RemoveIscsiStaticTarget"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RemoveIScsiStaticTargetW function


## -description


The <b>RemoveIscsiStaticTarget</b> function removes a target from the list of static targets made available to the machine.


## -parameters




### -param TargetName [in]

The name of the iSCSI target to remove from the static list. 


## -returns



Returns ERROR_SUCCESS if the operation succeeds. Otherwise, it returns the appropriate Win32 or iSCSI error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-addiscsistatictargeta">AddIscsiStaticTarget</a>
 

 

