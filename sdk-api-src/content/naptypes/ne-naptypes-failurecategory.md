---
UID: NE:naptypes.tagFailureCategory
title: FailureCategory (naptypes.h)
author: windows-sdk-content
description: Indicates the source of a failure.
old-location: nap\failurecategory_enum.htm
tech.root: NAP
ms.assetid: 3f528702-c9f3-4a91-960b-8b3f3eea91e9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FailureCategory, FailureCategory enumeration [NAP], failureCategoryClientCommunication, failureCategoryClientComponent, failureCategoryNone, failureCategoryOther, failureCategoryServerCommunication, failureCategoryServerComponent, nap.failurecategory_enum, naptypes/FailureCategory, naptypes/failureCategoryClientCommunication, naptypes/failureCategoryClientComponent, naptypes/failureCategoryNone, naptypes/failureCategoryOther, naptypes/failureCategoryServerCommunication, naptypes/failureCategoryServerComponent
ms.topic: enum
f1_keywords: 
 - "naptypes/FailureCategory"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - NapTypes.h
api_name:
 - FailureCategory
targetos: Windows
req.typenames: FailureCategory
req.redist: 
ms.custom: 19H1
---

# FailureCategory enumeration


## -description


<div class="alert"><b>Note</b>  The Network Access Protection platform is not available starting with Windows 10</div><div> </div>The <b>FailureCategory</b> enumeration indicates the source of a failure.


## -enum-fields




### -field failureCategoryNone

No failure.


### -field failureCategoryOther

A failure which is not due to client or server components or communications.


### -field failureCategoryClientComponent

Failure due to client component.


### -field failureCategoryClientCommunication

Failure due to client communication.


### -field failureCategoryServerComponent

Failure due to server component.


### -field failureCategoryServerCommunication

Failure due to server communication.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/naptypes/ns-naptypes-failurecategorymapping">FailureCategoryMapping</a>
 

 

