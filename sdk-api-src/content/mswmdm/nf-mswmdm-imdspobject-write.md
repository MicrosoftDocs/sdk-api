---
UID: NF:mswmdm.IMDSPObject.Write
title: IMDSPObject::Write (mswmdm.h)
description: The Write method writes data to the object at the current position within the object. This operation is valid only if the storage object represents a file.
helpviewer_keywords: ["IMDSPObject interface [windows Media Device Manager]","Write method","IMDSPObject.Write","IMDSPObject::Write","IMDSPObjectWrite","Write","Write method [windows Media Device Manager]","Write method [windows Media Device Manager]","IMDSPObject interface","mswmdm/IMDSPObject::Write","wmdm.imdspobject_write"]
old-location: wmdm\imdspobject_write.htm
tech.root: WMDM
ms.assetid: 29f16be5-9304-4b09-86e8-3f9e0e591a41
ms.date: 12/05/2018
ms.keywords: IMDSPObject interface [windows Media Device Manager],Write method, IMDSPObject.Write, IMDSPObject::Write, IMDSPObjectWrite, Write, Write method [windows Media Device Manager], Write method [windows Media Device Manager],IMDSPObject interface, mswmdm/IMDSPObject::Write, wmdm.imdspobject_write
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
 - IMDSPObject::Write
 - mswmdm/IMDSPObject::Write
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
 - IMDSPObject.Write
---

# IMDSPObject::Write


## -description

The <b>Write</b> method writes data to the object at the current position within the object. This operation is valid only if the storage object represents a file.

## -parameters

### -param pData [in]

Pointer to the buffer containing the data to write to the object. This parameter is encrypted and must be decrypted using <a href="/previous-versions/bb231598(v=vs.85)">CSecureChannelServer::DecryptParam</a> with the MAC in <i>abMac</i>. See Remarks.

### -param pdwSize [in, out]

<b>DWORD</b> containing the number of bytes of data to write. Upon return, this parameter contains the actual number of bytes written. This parameter must be included in both the input and output message authentication codes.

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

This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="/windows/desktop/WMDM/mandatory-and-optional-interfaces">Mandatory and Optional Interfaces</a>.

## -see-also

<a href="/windows/desktop/WMDM/encryption-and-decryption">Encryption and Decryption</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject">IMDSPObject Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-close">IMDSPObject::Close</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-open">IMDSPObject::Open</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read">IMDSPObject::Read</a>