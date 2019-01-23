---
UID: NF:shobjidl_core.SHGetPropertyStoreFromIDList
title: SHGetPropertyStoreFromIDList function
author: windows-sdk-content
description: Retrieves an object that supports IPropertyStore or related interfaces from a pointer to an item identifier list (PIDL).
old-location: properties\SHGetPropertyStoreFromIDList.htm
tech.root: properties
ms.assetid: 2a3c3c80-1bfc-4da0-ba6e-ac9e9a5c3e5b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SHGetPropertyStoreFromIDList, SHGetPropertyStoreFromIDList function [Windows Properties], _shell_SHGetPropertyStoreFromIDList, properties.SHGetPropertyStoreFromIDList, shell.SHGetPropertyStoreFromIDList, shobjidl_core/SHGetPropertyStoreFromIDList
ms.topic: function
req.header: shobjidl_core.h
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
req.lib: 
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHGetPropertyStoreFromIDList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SHGetPropertyStoreFromIDList function


## -description


Retrieves an object that supports <a href="https://msdn.microsoft.com/en-us/library/Bb761474(v=VS.85).aspx">IPropertyStore</a> or related interfaces from a pointer to an item identifier list (PIDL).


## -parameters




### -param pidl [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

A pointer to an item ID list.


### -param flags [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb762582(v=VS.85).aspx">GETPROPERTYSTOREFLAGS</a></b>

One or more values from the <a href="https://msdn.microsoft.com/en-us/library/Bb762582(v=VS.85).aspx">GETPROPERTYSTOREFLAGS</a> constants. This parameter can also be <b>NULL</b>.


### -param riid [in]

Type: <b>REFIID</b>

A reference to the desired interface ID.


### -param ppv [out]

Type: <b>void**</b>

When this function returns, contains the interface pointer requested in <i>riid</i>. This is typically <a href="https://msdn.microsoft.com/en-us/library/Bb761474(v=VS.85).aspx">IPropertyStore</a> or a related interface. 

