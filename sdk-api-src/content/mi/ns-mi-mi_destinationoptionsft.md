---
UID: NS:mi._MI_DestinationOptionsFT
title: MI_DestinationOptionsFT (mi.h)
author: windows-sdk-content
description: A support structure used in the MI_DestinationOptions structure. Use the functions with the name prefix &#0034;MI_DestinationOptions_&#0034; to manipulate these structures.
old-location: wmi_v2\mi_destinationoptionsft.htm
tech.root: wmi_v2
ms.assetid: e6cf4d82-8820-40d5-924a-e4270252807d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MI_DestinationOptionsFT, MI_DestinationOptionsFT structure [Windows Management Infrastructure (MI)], mi/MI_DestinationOptionsFT, wmi_v2.mi_destinationoptionsft
ms.topic: struct
f1_keywords:
- mi/MI_DestinationOptionsFT
dev_langs:
 - c++
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
- Mi.h
api_name:
- MI_DestinationOptionsFT
targetos: Windows
req.typenames: MI_DestinationOptionsFT
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
---

# MI_DestinationOptionsFT structure


## -description


A support structure used in the <a href="https://docs.microsoft.com/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a> structure.  Use the functions with the name prefix "MI_DestinationOptions_" to manipulate these structures.


## -struct-fields




### -field MI_Result

TBD 




#### - AddCredentials

Used internally.


#### - Clone

Creates a copy of a <a href="https://docs.microsoft.com/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a> structure. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_destinationoptions_clone">MI_DestinationOptions_Clone</a>.


#### - Delete

Deletes the destination options created by using <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a>. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_destinationoptions_delete">MI_DestinationOptions_Delete</a>.


#### - GetCredentialsAt

Get the credentials at the specified index. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_destinationoptions_getcredentialsat">MI_DestinationOptions_GetCredentialsAt</a>.


#### - GetCredentialsCount

Gets the number of previously added credentials. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_destinationoptions_getcredentialscount">MI_DestinationOptions_GetCredentialsCount</a>.


#### - GetCredentialsPasswordAt

Gets a credentials password based on a specified index. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_destinationoptions_getcredentialspasswordat">MI_DestinationOptions_GetCredentialsPasswordAt</a>.


#### - GetNumber

Gets a previously added custom number option. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_destinationoptions_getnumber">MI_DestinationOptions_GetNumber</a>.


#### - GetOption

Gets a previously added option value based on the option name. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_destinationoptions_getoption">MI_DestinationOptions_GetOption</a>.


#### - GetOptionAt

Gets a previously added option value based on the specified index. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_destinationoptions_getoptionat">MI_DestinationOptions_GetOptionAt</a>.


#### - GetOptionCount

Gets the number of options previously added. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_destinationoptions_getoptioncount">MI_DestinationOptions_GetOptionCount</a>.


#### - GetString

Gets a previously added custom string option. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_destinationoptions_getstring">MI_DestinationOptions_GetString</a>.


#### - SetNumber

Sets a custom numeric option value. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_destinationoptions_setnumber">MI_DestinationOptions_SetNumber</a>.


#### - SetString

Sets a custom string option. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_destinationoptions_setstring">MI_DestinationOptions_SetString</a>.

