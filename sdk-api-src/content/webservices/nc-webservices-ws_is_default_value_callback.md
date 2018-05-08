---
UID: NC:webservices.WS_IS_DEFAULT_VALUE_CALLBACK
title: WS_IS_DEFAULT_VALUE_CALLBACK
author: windows-driver-content
description: Determines if a value is the default value.
old-location: wsw\ws_is_default_value_callback.htm
old-project: wsw
ms.assetid: 1bfbd405-860e-4888-8363-bbc678d1256a
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: WS_IS_DEFAULT_VALUE_CALLBACK, WS_IS_DEFAULT_VALUE_CALLBACK callback, WS_IS_DEFAULT_VALUE_CALLBACK callback function [Web Services for Windows], webservices/WS_IS_DEFAULT_VALUE_CALLBACK, wsw.ws_is_default_value_callback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WDSTRANSPORT_TFTP_CAPABILITY, *PWDSTRANSPORT_TFTP_CAPABILITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	WebServices.h
api_name:
-	WS_IS_DEFAULT_VALUE_CALLBACK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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



