---
UID: NF:shobjidl_core.IShellFolder2.EnumSearches
title: IShellFolder2::EnumSearches
author: windows-driver-content
description: Requests a pointer to an interface that allows a client to enumerate the available search objects.
old-location: shell\IShellFolder2_EnumSearches.htm
old-project: shell
ms.assetid: ed7b0e3c-f679-491b-98a2-542fcf5d2077
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: EnumSearches, EnumSearches method [Windows Shell], EnumSearches method [Windows Shell],IShellFolder2 interface, IShellFolder2 interface [Windows Shell],EnumSearches method, IShellFolder2.EnumSearches, IShellFolder2::EnumSearches, _win32_IShellFolder2_EnumSearches, shell.IShellFolder2_EnumSearches, shobjidl_core/IShellFolder2::EnumSearches
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	IShellFolder2.EnumSearches
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IShellFolder2::EnumSearches


## -description


Requests a pointer to an interface that allows a client to enumerate the available search objects.


## -parameters




### -param ppenum






#### - ppEnum

Type: <b><a href="https://msdn.microsoft.com/63b71cd2-483b-482f-b3f4-6d5c937e7708">IEnumExtraSearch</a>**</b>


          The address of a pointer to an enumerator object's <a href="https://msdn.microsoft.com/63b71cd2-483b-482f-b3f4-6d5c937e7708">IEnumExtraSearch</a> interface.
        


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM error value otherwise.



