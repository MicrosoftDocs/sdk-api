---
UID: NF:iscsidsc.RemoveIScsiStaticTargetW
title: RemoveIScsiStaticTargetW function (iscsidsc.h)
author: windows-sdk-content
description: RemoveIscsiStaticTarget function removes a target from the list of static targets made available to the machine.
old-location: iscsidisc\removeiscsistatictarget.htm
tech.root: iSCSIDisc
ms.assetid: 7927d414-929e-4f01-b6bf-e6d571486aed
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RemoveIScsiStaticTargetW, RemoveIscsiStaticTarget, RemoveIscsiStaticTarget function [iSCSI Discovery Library API], RemoveIscsiStaticTargetA, RemoveIscsiStaticTargetW, iscsidisc.removeiscsistatictarget, iscsidsc/RemoveIscsiStaticTarget, iscsidsc/RemoveIscsiStaticTargetA, iscsidsc/RemoveIscsiStaticTargetW
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/81f5ac9a-debb-4fa3-8ccf-1303cd45f1de">AddIscsiStaticTarget</a>
 

 

