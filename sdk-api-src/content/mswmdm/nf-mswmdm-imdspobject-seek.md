---
UID: NF:mswmdm.IMDSPObject.Seek
title: IMDSPObject::Seek (mswmdm.h)
description: The Seek method sets the current position within the object. This operation is valid only if the storage object represents a file.
old-location: wmdm\imdspobject_seek.htm
tech.root: WMDM
ms.assetid: 89494180-9dd7-41f3-b510-a59c38415d75
ms.date: 12/05/2018
ms.keywords: IMDSPObject interface [windows Media Device Manager],Seek method, IMDSPObject.Seek, IMDSPObject::Seek, IMDSPObjectSeek, Seek, Seek method [windows Media Device Manager], Seek method [windows Media Device Manager],IMDSPObject interface, mswmdm/IMDSPObject::Seek, wmdm.imdspobject_seek
f1_keywords:
- mswmdm/IMDSPObject.Seek
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
- IMDSPObject.Seek
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMDSPObject::Seek


## -description



The <b>Seek</b> method sets the current position within the object. This operation is valid only if the storage object represents a file.




## -parameters




### -param fuFlags [in]

Mode in which the file must be opened. It must be one of the values in the following table.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>MDSP_SEEK_BOF</td>
<td>Seek <i>dwOffset</i> bytes forward from the beginning of the file.</td>
</tr>
<tr>
<td>MDSP_SEEK_CUR</td>
<td>Seek <i>dwOffset</i> bytes forward from the current position.</td>
</tr>
<tr>
<td>MDSP_SEEK_EOF</td>
<td>Seek <i>dwOffset</i> bytes backward from the end of the file.</td>
</tr>
</table>
 


### -param dwOffset [in]

<b>DWORD</b> containing the number of bytes to seek.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://docs.microsoft.com/windows/desktop/WMDM/error-codes">Error Codes</a>.




## -remarks



This method is optional. For more information, see <a href="https://docs.microsoft.com/windows/desktop/WMDM/mandatory-and-optional-interfaces">Mandatory and Optional Interfaces</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject">IMDSPObject Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-open">IMDSPObject::Open</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read">IMDSPObject::Read</a>
 

 

