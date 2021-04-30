---
UID: NF:mswmdm.IMDSPObject.Read
title: IMDSPObject::Read (mswmdm.h)
description: The Read method reads data from the object at the current position. This operation is valid only if the storage object represents a file.
helpviewer_keywords: ["IMDSPObject interface [windows Media Device Manager]","Read method","IMDSPObject.Read","IMDSPObject::Read","IMDSPObjectRead","Read","Read method [windows Media Device Manager]","Read method [windows Media Device Manager]","IMDSPObject interface","mswmdm/IMDSPObject::Read","wmdm.imdspobject_read"]
old-location: wmdm\imdspobject_read.htm
tech.root: WMDM
ms.assetid: 1acf4112-0cb8-47e4-b8dc-3e820c0ef72f
ms.date: 12/05/2018
ms.keywords: IMDSPObject interface [windows Media Device Manager],Read method, IMDSPObject.Read, IMDSPObject::Read, IMDSPObjectRead, Read, Read method [windows Media Device Manager], Read method [windows Media Device Manager],IMDSPObject interface, mswmdm/IMDSPObject::Read, wmdm.imdspobject_read
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMDSPObject::Read
 - mswmdm/IMDSPObject::Read
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IMDSPObject.Read
---

# IMDSPObject::Read


## -description

The <b>Read</b> method reads data from the object at the current position. This operation is valid only if the storage object represents a file.

## -parameters

### -param pData [out]

Pointer to a buffer to receive the data read from the object. This parameter is included in the output message authentication code and must be encrypted using <a href="/previous-versions/ms868509(v=msdn.10)">CSecureChannelServer::EncryptParam</a>. See Remarks.

### -param pdwSize [in, out]

Pointer to a <b>DWORD</b> specifying the number of bytes of data to read. Upon return, this parameter contains the actual amount of data read. This parameter must be included in the input message authentication code.

### -param abMac [in, out]

Array of eight bytes containing the message authentication code for the parameter data of this method. (WMDM_MAC_LENGTH is defined as 8.)

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

The MAC used for encryption should include both <i>pData</i> and <i>pdwSize</i> in calls to <a href="/previous-versions/ms868515(v=msdn.10)">CSecureChannelServer::MACUpdate</a>.

This method is optional. For more information, see <a href="/windows/desktop/WMDM/mandatory-and-optional-interfaces">Mandatory and Optional Interfaces</a>.

## -see-also

<a href="/windows/desktop/WMDM/encryption-and-decryption">Encryption and Decryption</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject">IMDSPObject Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-close">IMDSPObject::Close</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-open">IMDSPObject::Open</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-seek">IMDSPObject::Seek</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write">IMDSPObject::Write</a>