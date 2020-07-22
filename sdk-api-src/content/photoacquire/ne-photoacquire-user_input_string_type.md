---
UID: NE:photoacquire.tagUSER_INPUT_STRING_TYPE
title: USER_INPUT_STRING_TYPE (photoacquire.h)
description: The USER_INPUT_STRING_TYPE enumeration type indicates the type of string to obtain from the user in IPhotoAcquireProgressCB::GetUserInput.
helpviewer_keywords: ["USER_INPUT_DEFAULT","USER_INPUT_PATH_ELEMENT","USER_INPUT_STRING_TYPE","USER_INPUT_STRING_TYPE enumeration [Picture Acquisition]","enumeration [Picture Acquisition]","photoacquire/USER_INPUT_DEFAULT","photoacquire/USER_INPUT_PATH_ELEMENT","photoacquire/USER_INPUT_STRING_TYPE","picacq.user_input_string_type"]
old-location: picacq\user_input_string_type.htm
tech.root: picacq
ms.assetid: ac05f51e-4762-4360-9c38-7baf84eeb1e9
ms.date: 12/05/2018
ms.keywords: USER_INPUT_DEFAULT, USER_INPUT_PATH_ELEMENT, USER_INPUT_STRING_TYPE, USER_INPUT_STRING_TYPE enumeration [Picture Acquisition], enumeration [Picture Acquisition], photoacquire/USER_INPUT_DEFAULT, photoacquire/USER_INPUT_PATH_ELEMENT, photoacquire/USER_INPUT_STRING_TYPE, picacq.user_input_string_type
f1_keywords:
- photoacquire/USER_INPUT_STRING_TYPE
dev_langs:
- c++
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
targetos: Windows
req.typenames: USER_INPUT_STRING_TYPE
req.redist: 
ms.custom: 19H1
---

# USER_INPUT_STRING_TYPE enumeration


## -description



The <code>USER_INPUT_STRING_TYPE</code> enumeration type indicates the type of string to obtain from the user in <a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireprogresscb-getuserinput">IPhotoAcquireProgressCB::GetUserInput</a>.




## -enum-fields




### -field USER_INPUT_DEFAULT

Indicates that any string is allowed.


### -field USER_INPUT_PATH_ELEMENT

Indicates that the string will not accept characters that are illegal in file or directory names (such as * or /).


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/acquisition/enumeration-types">Enumeration Types</a>



<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireprogresscb-getuserinput">IPhotoAcquireProgressCB::GetUserInput</a>



<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iuserinputstring-getstringtype">IUserInputString::GetStringType</a>
 

 

