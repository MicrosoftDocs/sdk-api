---
UID: NF:shobjidl_core.IEnumExtraSearch.Clone
title: IEnumExtraSearch::Clone
author: windows-sdk-content
description: Used to request a duplicate of the enumerator object to preserve its current state.
old-location: shell\IEnumExtraSearch_Clone.htm
old-project: shell
ms.assetid: 9d766cf9-784b-4e89-ad58-bab6415630fe
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: Clone, Clone method [Windows Shell], Clone method [Windows Shell],IEnumExtraSearch interface, IEnumExtraSearch interface [Windows Shell],Clone method, IEnumExtraSearch.Clone, IEnumExtraSearch::Clone, _win32_IEnumExtraSearch_Clone, shell.IEnumExtraSearch_Clone, shobjidl_core/IEnumExtraSearch::Clone
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IEnumExtraSearch.Clone
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IEnumExtraSearch::Clone


## -description


Used to request a duplicate of the enumerator object to preserve its current state.


## -parameters




### -param ppenum






#### - ppEnum

Type: <b><a href="https://msdn.microsoft.com/63b71cd2-483b-482f-b3f4-6d5c937e7708">IEnumExtraSearch</a>**</b>

A pointer to the <a href="https://msdn.microsoft.com/63b71cd2-483b-482f-b3f4-6d5c937e7708">IEnumExtraSearch</a> interface of a new enumerator object.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM-defined error code otherwise.




## -remarks



The new enumerator should be created with the same state as the current one. Use the <a href="https://msdn.microsoft.com/f77983e2-bae4-4350-8950-b4e76fc46365">IEnumExtraSearch::Skip</a> method to advance the enumeration index to the appropriate value before returning.



