---
UID: NF:oleauto.CreateTypeLib2
title: CreateTypeLib2 function
author: windows-sdk-content
description: Creates a type library in the current file format.
old-location: automat\createtypelib2.htm
tech.root: automat
ms.assetid: 73df6ef2-fae1-4cfb-ba59-3812e3a2e3b9
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CreateTypeLib2, CreateTypeLib2 function [Automation], _oa96_CreateTypeLib2, automat.createtypelib2, oleauto/CreateTypeLib2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: oleauto.h
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
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - CreateTypeLib2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateTypeLib2 function


## -description


Creates a type library in the current file format.

The file and in-memory format for the current version of Automation makes use of memory-mapped files. The <a href="https://msdn.microsoft.com/c7a94d5b-7ac5-4b7c-8aed-ead23de9ea75">CreateTypeLib</a> function is still available for creating a type library in the older format.


## -parameters




### -param syskind

The target operating system for which to create a type library.




### -param szFile

The name of the file to create.




### -param ppctlib

The <a href="https://msdn.microsoft.com/97378353-8c2d-493a-8ee9-42d33ab47d18">ICreateTypeLib2</a> interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



