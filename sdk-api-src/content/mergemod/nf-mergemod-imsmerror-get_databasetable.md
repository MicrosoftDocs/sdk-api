---
UID: NF:mergemod.IMsmError.get_DatabaseTable
title: IMsmError::get_DatabaseTable
author: windows-sdk-content
description: The read-only DatabaseTable property of the Error object returns the name of the table in the database that caused the error.
old-location: setup\error_databasetable.htm
old-project: msi
ms.assetid: 38ff45ca-4bd6-43f3-88ad-db4077daeb77
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: DatabaseTable property, DatabaseTable property,Error object, Error object,DatabaseTable property, Error.DatabaseTable, IMsmError.get_DatabaseTable, IMsmError::get_DatabaseTable, _msi_databasetable_property, get_DatabaseTable, setup.error_databasetable
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
 - Error.DatabaseTable
 - IMsmError.get_DatabaseTable
product: Windows
targetos: Windows
req.lib: 
req.dll: Mergemod.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMsmError::get_DatabaseTable


## -description


The read-only 
<b>DatabaseTable</b> property of the 
<a href="https://msdn.microsoft.com/38025e21-2d31-40f8-a088-2d3912c2893e">Error</a> object returns the name of the table in the database that caused the error.

This property is read-only.


## -parameters


## -remarks



The collection is empty if the values do not apply to the type of the error. You can determine the type of error by calling 
<a href="https://msdn.microsoft.com/5567ba71-c815-4434-962c-aa46cd171712">Type</a> property of the 
<a href="https://msdn.microsoft.com/38025e21-2d31-40f8-a088-2d3912c2893e">Error</a> object.

<h3><a id="C__"></a><a id="c__"></a>C++</h3>
See 
<a href="https://msdn.microsoft.com/fee774b3-66ee-4ffd-b000-8032118e9a9d">get_DatabaseTable</a> function.



