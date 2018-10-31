---
UID: NF:shlwapi.StrRetToBSTR
title: StrRetToBSTR function
author: windows-sdk-content
description: Accepts a STRRET structure returned by IShellFolder::GetDisplayNameOf that contains or points to a string, and returns that string as a BSTR.
old-location: shell\StrRetToBSTR.htm
tech.root: shell
ms.assetid: 2a5a9a2b-74df-4521-a5b2-8fc91c3559eb
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: StrRetToBSTR, StrRetToBSTR function [Windows Shell], _shell_StrRetToBSTR, shell.StrRetToBSTR, shlwapi/StrRetToBSTR
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.5 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
api_name:
 - StrRetToBSTR
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# StrRetToBSTR function


## -description


Accepts a <a href="https://msdn.microsoft.com/7868ef9b-07db-455b-b0be-ef0db7891447">STRRET</a> structure returned by <a href="https://msdn.microsoft.com/2164bbe6-e030-4a64-85db-9ee1cd3c136d">IShellFolder::GetDisplayNameOf</a> that contains or points to a string, and returns that string as a <a href="1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a>.


## -parameters




### -param pstr [in, out]

Type: <b><a href="https://msdn.microsoft.com/7868ef9b-07db-455b-b0be-ef0db7891447">STRRET</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/7868ef9b-07db-455b-b0be-ef0db7891447">STRRET</a> structure. When the function returns, this pointer is longer valid.


### -param pidl [in]

Type: <b>PCUITEMID_CHILD</b>

A pointer to an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> that uniquely identifies a file object or subfolder relative to the parent folder. This value can be <b>NULL</b>.


### -param pbstr [out]

Type: <b><a href="1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a>*</b>

A pointer to a variable of type <a href="1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a> that receives the converted string.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the <i>uType</i> member of the <a href="https://msdn.microsoft.com/7868ef9b-07db-455b-b0be-ef0db7891447">STRRET</a> structure pointed to by <i>pstr</i> is set to <b>STRRET_WSTR</b>, the <i>pOleStr</i> member of that structure is freed on return.




## -see-also




<a href="https://msdn.microsoft.com/2164bbe6-e030-4a64-85db-9ee1cd3c136d">IShellFolder::GetDisplayNameOf</a>



<a href="https://msdn.microsoft.com/89dab3ee-e9f8-499a-97ec-6fe732315891">StrRetToBuf</a>



<a href="https://msdn.microsoft.com/03b0dffb-8ef7-41da-9773-81ed55275802">StrRetToStr</a>
 

 

