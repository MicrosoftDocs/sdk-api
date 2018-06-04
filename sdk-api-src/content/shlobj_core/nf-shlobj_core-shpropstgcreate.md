---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# SHPropStgCreate function


## -description


<p class="CCE_Message">[This function is available through Windows XP Service Pack 2 (SP2) and Windows Server 2003. It might be altered or unavailable in subsequent versions of Windows.]

Ensures proper handling of code page retrieval or assignment for the requested property set operation.


## -parameters




### -param psstg [in]

Type: <b><a href="https://msdn.microsoft.com/0ea3e1e0-c135-4138-81e4-f72412fc3128">IPropertySetStorage</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/0ea3e1e0-c135-4138-81e4-f72412fc3128">IPropertySetStorage</a> interface.


### -param fmtid [in]

Type: <b>REFFMTID</b>

A property set ID to open. The values for this parameter can be either one of those defined in <a href="https://msdn.microsoft.com/cc99ce1b-beb5-4340-91ed-3aed5bdad2bd">Predefined Property Set Format Identifiers</a> or any other FMTID that you register.


### -param pclsid [in, optional]

Type: <b>const CLSID*</b>

A pointer to the CLSID associated with the set. This parameter can be <b>NULL</b>.


### -param grfFlags

Type: <b>DWORD</b>

One or more members of the <a href="stg.propsetflag">PROPSETFLAG</a> enumeration that determine how the property set is created and opened. All sets containing ANSI bytes should be created with PROPSETFLAG_ANSI, otherwise PROPSETFLAG_DEFAULT.


### -param grfMode

Type: <b>DWORD</b>

The flags from the <a href="stg.stgm">STGM</a> enumeration that indicate conditions for creating and deleting the object and access modes for the object. Must contain STGM_DIRECT | STGM_SHARE_EXCLUSIVE.


### -param dwDisposition

Type: <b>DWORD</b>

One of the following values, defined in Fileapi.h.



#### CREATE_NEW (1)

Create a new set if one does not already exist.



#### CREATE_ALWAYS (2)

Always create a new set, overwriting any existing set.



#### OPEN_EXISTING (3)

Open the existing set.



#### OPEN_ALWAYS (4)


### -param ppstg [out]

Type: <b><a href="https://msdn.microsoft.com/c021f695-db54-4861-9f30-35a81d2dccd5">IPropertyStorage</a>**</b>

When this method returns, contains an <a href="https://msdn.microsoft.com/c021f695-db54-4861-9f30-35a81d2dccd5">IPropertyStorage</a> interface pointer.


### -param puCodePage [out, optional]

Type: <b>UINT*</b>

When this method returns, contains the address of the code page ID for the set.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



