---
UID: NF:mergemod.IMsmError.get_DatabaseKeys
title: IMsmError::get_DatabaseKeys
author: windows-sdk-content
description: The read-only DatabaseKeys property of the Error object returns a string collection that contains the primary keys of the database row causing the error. There is one key per entry in the collection.
old-location: setup\error_databasekeys.htm
old-project: msi
ms.assetid: 416a6cef-4c70-4c06-a8d2-801c9440e25a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DatabaseKeys property, DatabaseKeys property,Error object, Error object,DatabaseKeys property, Error.DatabaseKeys, IMsmError.get_DatabaseKeys, IMsmError::get_DatabaseKeys, _msi_databasekeys_property, get_DatabaseKeys, setup.error_databasekeys
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mergemod.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Mergemod.dll 1.0 or later
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
tech.root: 
req.typenames: WIN32_MEMORY_REGION_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mergemod.dll
api_name:
 - Error.DatabaseKeys
 - IMsmError.get_DatabaseKeys
product: Windows
targetos: Windows
req.lib: 
req.dll: Mergemod.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMsmError::get_DatabaseKeys


## -description


The read-only 
<b>DatabaseKeys</b> property of the 
<a href="https://msdn.microsoft.com/38025e21-2d31-40f8-a088-2d3912c2893e">Error</a> object returns a string collection that contains the primary keys of the database row causing the error. There is one key per entry in the collection.

This property is read-only.


## -parameters


## -remarks



The client is responsible for releasing the string collection when it is no longer needed.

The collection is empty if the values do not apply to the type of the error. You can determine the type of error by calling the 
<a href="https://msdn.microsoft.com/5567ba71-c815-4434-962c-aa46cd171712">Type</a> property of the 
<a href="https://msdn.microsoft.com/38025e21-2d31-40f8-a088-2d3912c2893e">Error</a> object.

<h3><a id="C__"></a><a id="c__"></a>C++</h3>
See 
<a href="https://msdn.microsoft.com/7c256f03-208c-4adf-9b57-7648064f0dce">get_DatabaseKeys</a> function.



