---
UID: NF:winevt.EvtOpenPublisherMetadata
title: EvtOpenPublisherMetadata function
author: windows-sdk-content
description: Gets a handle that you use to read the specified provider's metadata.
old-location: wes\evtopenpublishermetadata.htm
tech.root: WES
ms.assetid: 0839fb15-12a9-4e30-9afa-6f6437956df0
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: EvtOpenPublisherMetadata, EvtOpenPublisherMetadata function [EventLog], wes.evtopenpublishermetadata, winevt/EvtOpenPublisherMetadata
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winevt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wevtapi.lib
req.dll: Wevtapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wevtapi.dll
 - Ext-MS-Win-WevtAPI-EventLog-L1-1-2.dll
api_name:
 - EvtOpenPublisherMetadata
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EvtOpenPublisherMetadata function


## -description


Gets a handle that you use to read the specified provider's metadata.


## -parameters




### -param Session [in, optional]

A remote session handle that the <a href="https://msdn.microsoft.com/26f1745c-dcca-4452-872e-1fffe20f049c">EvtOpenSession</a> function returns. Set to <b>NULL</b> to get the metadata for a provider on the local computer.


### -param PublisherId [in]

The name of the provider. To enumerate the names of the providers registered on the computer, call the <a href="https://msdn.microsoft.com/156c434c-6d0f-4af0-bf10-20aa6bae0945">EvtOpenPublisherEnum</a> function.


### -param LogFilePath [in, optional]

The full path to an archived log file that contains the events that the provider logged. An archived log file also contains the provider's metadata. Use this parameter when the provider is not registered on the local computer. Set to <b>NULL</b> when reading the metadata from a registered provider..


### -param Locale [in]

The locale identifier to use when accessing the localized metadata from the provider. To create the locale identifier, use the MAKELCID macro. Set to 0 to use the locale identifier of the calling thread.


### -param Flags [in]

Reserved. Must be zero.


## -returns



If successful, the function returns a handle to the provider's metadata; otherwise, <b>NULL</b>. If <b>NULL</b>, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function to get the error code.




## -remarks



 If you specify an archived log file, this function will check for the specified provider's metadata in the log file. If the provider's metadata is not found in the log file, the function will search for the provider in the list of registered providers on the local computer.

To read the provider's metadata, call the <a href="https://msdn.microsoft.com/f85a46ef-873c-4dd9-8b5c-3763fd67fc06">EvtGetPublisherMetadataProperty</a> function. To enumerate the events that the provider defines, call the <a href="https://msdn.microsoft.com/e1d2e5d5-89db-4bda-9803-37f26d1fe30f">EvtOpenEventMetadataEnum</a> function.

You must call the <a href="https://msdn.microsoft.com/c4b82d7b-508d-45bf-b990-04e90e846525">EvtClose</a> function to close the metadata handle when done.


#### Examples

For an example that shows how to use this function, see <a href="https://msdn.microsoft.com/c9442dc1-3599-4e81-a144-943c2843a2f7">Getting a Provider's Metadata</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/f85a46ef-873c-4dd9-8b5c-3763fd67fc06">EvtGetPublisherMetadataProperty</a>



<a href="https://msdn.microsoft.com/e1d2e5d5-89db-4bda-9803-37f26d1fe30f">EvtOpenEventMetadataEnum</a>



<a href="https://msdn.microsoft.com/156c434c-6d0f-4af0-bf10-20aa6bae0945">EvtOpenPublisherEnum</a>
 

 

