---
UID: NF:shlobj_core.IDListContainerIsConsistent
title: IDListContainerIsConsistent function
author: windows-driver-content
description: Verifies that the container structure of an IDList is valid.
old-location: shell\IDListContainerIsConsistent.htm
old-project: shell
ms.assetid: 2B61EDB2-F967-450a-9294-4A6597859F2C
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: IDListContainerIsConsistent, IDListContainerIsConsistent function [Windows Shell], shell.IDListContainerIsConsistent, shlobj_core/IDListContainerIsConsistent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h
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
req.typenames: AUTOCOMPLETELISTOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	shlobj_core.h
api_name:
-	IDListContainerIsConsistent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# IDListContainerIsConsistent function


## -description


Verifies that the container structure of an IDList is valid.


## -parameters




### -param pidl [in]

A pointer to the IDList to validate.


### -param cbAlloc [in]

The size, in bytes, of the PIDL specified in the <i>pidl</i> parameter.


## -returns



<b>TRUE</b> if the IDList structure is valid; otherwise, <b>FALSE</b>.




## -remarks



This function should be used by any code that reads an IDList from a persisted format to ensure that invalid forms do not lead to a security exploit in the code that interprets the IDList. Shell data sources are responsible for validating private sections of the ITEMIDs. Hidden data is validated by the functions that interpret that data.



