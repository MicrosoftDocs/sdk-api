---
UID: NF:vds.IVdsService.QueryDriveLetters
title: IVdsService::QueryDriveLetters (vds.h)
description: Returns property details for a set of drive letters.
helpviewer_keywords: ["IVdsService interface [VDS]","QueryDriveLetters method","IVdsService.QueryDriveLetters","IVdsService::QueryDriveLetters","QueryDriveLetters","QueryDriveLetters method [VDS]","QueryDriveLetters method [VDS]","IVdsService interface","base.ivdsservice_querydriveletters","vds/IVdsService::QueryDriveLetters"]
old-location: base\ivdsservice_querydriveletters.htm
tech.root: base
ms.assetid: e9e9f8b0-963f-4c57-9553-8b9241317b55
ms.date: 12/05/2018
ms.keywords: IVdsService interface [VDS],QueryDriveLetters method, IVdsService.QueryDriveLetters, IVdsService::QueryDriveLetters, QueryDriveLetters, QueryDriveLetters method [VDS], QueryDriveLetters method [VDS],IVdsService interface, base.ivdsservice_querydriveletters, vds/IVdsService::QueryDriveLetters
f1_keywords:
- vds/IVdsService.QueryDriveLetters
dev_langs:
- c++
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: Uuid.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Uuid.lib
- Uuid.dll
api_name:
- IVdsService.QueryDriveLetters
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsService::QueryDriveLetters


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns property details for a set of drive letters. 


## -parameters




### -param wcFirstLetter [in]

The first drive letter to retrieve.


### -param count [in]

The total number of drive letters to retrieve.


### -param pDriveLetterPropArray [out]

The address of an array of <a href="https://docs.microsoft.com/windows/desktop/api/vds/ns-vds-vds_drive_letter_prop">VDS_DRIVE_LETTER_PROP</a> structures. The size of the array is <i>count</i>. Callers must allocate the memory for this array.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="https://docs.microsoft.com/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://docs.microsoft.com/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_INITIALIZED_FAILED</b></dt>
<dt>0x80042401L</dt>
</dl>
</td>
<td width="60%">
VDS failed to initialize. If an application calls this method before the service finishes initializing, the method is blocked until the initialization completes. If the initialization fails, this error is returned.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vds/nn-vds-ivdsservice">IVdsService</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vds/ns-vds-vds_drive_letter_prop">VDS_DRIVE_LETTER_PROP</a>
 

 

