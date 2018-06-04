---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# WS_IS_DEFAULT_VALUE_CALLBACK callback function


## -description



                Determines if a value is the default value. This callback is used  before a value that is handled
                by a <a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_CUSTOM_TYPE</a> is serialized.  Support
                for default values is enabled by specifying 
                when <a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONAL</a> in the <a href="https://msdn.microsoft.com/8b562fab-f3c5-4732-b993-f7f61ca14ab6">WS_FIELD_DESCRIPTION</a>.
            


## -parameters




### -param *descriptionData [in]


                    This is the value of the descriptionData field from <a href="https://msdn.microsoft.com/7ae3d16c-0755-4226-844e-52cf96fa84fb">WS_CUSTOM_TYPE_DESCRIPTION</a>.
                    The callback can use this to access any additional information about the type.
                


### -param *value


                    A pointer to the value being serialized.
                


### -param *defaultValue


                    A pointer to the default value.  If no default value was specified
                    for the field, this parameter will be <b>NULL</b>.
                


                    If the parameter is non-<b>NULL</b>, the callback should compare the two 
                    values field-by-field according to the custom type.  If the 
                    fields match, then the isDefault parameter should be set to <b>TRUE</b>.
                


                    If the parameter is <b>NULL</b>, the callback should compare the fields
                    of the value with zero.  If the fields match, then the isDefault
                    parameter should be set to <b>TRUE</b>.
                


### -param valueSize [in]


                    The size, in bytes, of the value being serialized.
                


### -param *isDefault [out]


                    Whether or not the value is the default value.
                


### -param *error [in, optional]


                    Specifies where additional error information should be stored if the function fails.
                


## -returns



This callback function does not return a value.



