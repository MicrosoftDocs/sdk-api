---
UID: NF:mswmdm.IMDSPStorage.GetRights
title: IMDSPStorage::GetRights (mswmdm.h)
description: The GetRights method retrieves the rights information for an object.helpviewer_keywords: ["GetRights","GetRights method [windows Media Device Manager]","GetRights method [windows Media Device Manager]","IMDSPStorage interface","IMDSPStorage interface [windows Media Device Manager]","GetRights method","IMDSPStorage.GetRights","IMDSPStorage::GetRights","IMDSPStorageGetRights","mswmdm/IMDSPStorage::GetRights","wmdm.imdspstorage_getrights"]
old-location: wmdm\imdspstorage_getrights.htm
tech.root: WMDM
ms.assetid: b4fb3ace-ebb5-4d95-8fce-780b5dc8e21a
ms.date: 12/05/2018
ms.keywords: GetRights, GetRights method [windows Media Device Manager], GetRights method [windows Media Device Manager],IMDSPStorage interface, IMDSPStorage interface [windows Media Device Manager],GetRights method, IMDSPStorage.GetRights, IMDSPStorage::GetRights, IMDSPStorageGetRights, mswmdm/IMDSPStorage::GetRights, wmdm.imdspstorage_getrights
f1_keywords:
- mswmdm/IMDSPStorage.GetRights
dev_langs:
- c++
req.header: mswmdm.h
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
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mssachlp.lib
- mssachlp.dll
api_name:
- IMDSPStorage.GetRights
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMDSPStorage::GetRights


## -description



The <b>GetRights</b> method retrieves the rights information for an object.




## -parameters




### -param ppRights [out]

Pointer to an array of <b>WMDMRIGHTS</b> structures that contain the storage object rights information. This parameter is included in the output message authentication code.


### -param pnRightsCount [out]

Pointer to the number of <b>WMDMRIGHTS</b> structures in the <i>ppRights</i> array. This parameter is included in the output message authentication code.


### -param abMac [in, out]

Array of eight bytes containing the message authentication code for the parameter data of this method. (WMDM_MAC_LENGTH is defined as 8.)


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://docs.microsoft.com/windows/desktop/WMDM/error-codes">Error Codes</a>.




## -remarks



Object rights describe the usage permissions for media content. For example, the <b>WMDMRIGHTS</b> structure can contain information concerning how many times a file can be played and who can play it.

The <i>ppRights</i> array is allocated by this method, and must be freed by the application using <b>CoTaskMemFree</b>, a standard Win32 function.

This method is optional. For more information, see <a href="https://docs.microsoft.com/windows/desktop/WMDM/mandatory-and-optional-interfaces">Mandatory and Optional Interfaces</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage">IMDSPStorage Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMDM/wmdmrights">WMDMRIGHTS</a>
 

 

