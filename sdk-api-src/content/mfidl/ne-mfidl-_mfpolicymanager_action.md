---
UID: NE:mfidl._MFPOLICYMANAGER_ACTION
title: "_MFPOLICYMANAGER_ACTION"
author: windows-sdk-content
description: Defines actions that can be performed on a stream.
old-location: mf\mfpolicymanager_action.htm
tech.root: medfound
ms.assetid: 74cee983-e084-458b-b615-5447cca9abbc
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: 74cee983-e084-458b-b615-5447cca9abbc, MFPOLICYMANAGER_ACTION, MFPOLICYMANAGER_ACTION enumeration [Media Foundation], PEACTION_COPY, PEACTION_EXPORT, PEACTION_EXTRACT, PEACTION_LAST, PEACTION_NO, PEACTION_PLAY, PEACTION_RESERVED1, PEACTION_RESERVED2, PEACTION_RESERVED3, _MFPOLICYMANAGER_ACTION, mf.mfpolicymanager_action, mfidl/MFPOLICYMANAGER_ACTION, mfidl/PEACTION_COPY, mfidl/PEACTION_EXPORT, mfidl/PEACTION_EXTRACT, mfidl/PEACTION_LAST, mfidl/PEACTION_NO, mfidl/PEACTION_PLAY, mfidl/PEACTION_RESERVED1, mfidl/PEACTION_RESERVED2, mfidl/PEACTION_RESERVED3
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - mfidl.h
api_name:
 - MFPOLICYMANAGER_ACTION
product: Windows
targetos: Windows
req.typenames: MFPOLICYMANAGER_ACTION
req.redist: 
---

# _MFPOLICYMANAGER_ACTION enumeration


## -description



Defines actions that can be performed on a stream.




## -enum-fields




### -field PEACTION_NO

No action.


### -field PEACTION_PLAY

Play the stream.


### -field PEACTION_COPY

Copy the stream.


### -field PEACTION_EXPORT

Export the stream to another format.


### -field PEACTION_EXTRACT

Extract the data from the stream and pass it to the application. For example, acoustic echo cancellation requires this action.


### -field PEACTION_RESERVED1

Reserved.


### -field PEACTION_RESERVED2

Reserved.


### -field PEACTION_RESERVED3

Reserved.


### -field PEACTION_LAST

Last member of the enumeration.


## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

