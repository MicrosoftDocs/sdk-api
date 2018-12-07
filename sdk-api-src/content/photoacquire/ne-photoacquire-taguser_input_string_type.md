---
UID: NE:photoacquire.tagUSER_INPUT_STRING_TYPE
title: tagUSER_INPUT_STRING_TYPE
author: windows-sdk-content
description: The USER_INPUT_STRING_TYPE enumeration type indicates the type of string to obtain from the user in IPhotoAcquireProgressCB::GetUserInput.
old-location: picacq\user_input_string_type.htm
tech.root: acquisition
ms.assetid: ac05f51e-4762-4360-9c38-7baf84eeb1e9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: USER_INPUT_DEFAULT, USER_INPUT_PATH_ELEMENT, USER_INPUT_STRING_TYPE, USER_INPUT_STRING_TYPE enumeration [Picture Acquisition], enumeration [Picture Acquisition], photoacquire/USER_INPUT_DEFAULT, photoacquire/USER_INPUT_PATH_ELEMENT, photoacquire/USER_INPUT_STRING_TYPE, picacq.user_input_string_type, tagUSER_INPUT_STRING_TYPE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: photoacquire.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - PhotoAcquire.h
api_name:
 - USER_INPUT_STRING_TYPE
product: Windows
targetos: Windows
req.typenames: USER_INPUT_STRING_TYPE
req.redist: 
---

# tagUSER_INPUT_STRING_TYPE enumeration


## -description



The <code>USER_INPUT_STRING_TYPE</code> enumeration type indicates the type of string to obtain from the user in <a href="https://msdn.microsoft.com/db0d924b-a586-4f81-a367-e8fbdf3e9bd9">IPhotoAcquireProgressCB::GetUserInput</a>.




## -enum-fields




### -field USER_INPUT_DEFAULT

Indicates that any string is allowed.


### -field USER_INPUT_PATH_ELEMENT

Indicates that the string will not accept characters that are illegal in file or directory names (such as * or /).


## -see-also




<a href="https://msdn.microsoft.com/767d20df-aeb4-4f86-a705-bfbb7dc254ff">Enumeration Types</a>



<a href="https://msdn.microsoft.com/db0d924b-a586-4f81-a367-e8fbdf3e9bd9">IPhotoAcquireProgressCB::GetUserInput</a>



<a href="https://msdn.microsoft.com/57f0c750-9c66-4c30-adc1-0cfd23d878d1">IUserInputString::GetStringType</a>
 

 

