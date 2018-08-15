---
UID: NE:naptypes.tagFailureCategory
title: tagFailureCategory
author: windows-sdk-content
description: Indicates the source of a failure.
old-location: nap\failurecategory_enum.htm
old-project: nap
ms.assetid: 3f528702-c9f3-4a91-960b-8b3f3eea91e9
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: FailureCategory, FailureCategory enumeration [NAP], failureCategoryClientCommunication, failureCategoryClientComponent, failureCategoryNone, failureCategoryOther, failureCategoryServerCommunication, failureCategoryServerComponent, nap.failurecategory_enum, naptypes/FailureCategory, naptypes/failureCategoryClientCommunication, naptypes/failureCategoryClientComponent, naptypes/failureCategoryNone, naptypes/failureCategoryOther, naptypes/failureCategoryServerCommunication, naptypes/failureCategoryServerComponent, tagFailureCategory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: naptypes.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LoadMUILibraryW (Unicode) and LoadMUILibraryA (ANSI)
req.idl: NapTypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: FailureCategory
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - NapTypes.h
api_name:
 - FailureCategory
product: Windows
targetos: Windows
req.lib: Muiload.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# tagFailureCategory enumeration


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




<a href="https://msdn.microsoft.com/dbf2978f-062a-417b-a6df-a82879e10ec8">FailureCategoryMapping</a>
 

 

