---
UID: NF:mswmdm.IMDSPObject2.WriteOnClearChannel
title: IMDSPObject2::WriteOnClearChannel (mswmdm.h)
description: The WriteOnClearChannel method writes data to the object to the current position within the object, without using secure authenticated channels.
helpviewer_keywords: ["IMDSPObject2 interface [windows Media Device Manager]","WriteOnClearChannel method","IMDSPObject2.WriteOnClearChannel","IMDSPObject2::WriteOnClearChannel","IMDSPObject2WriteOnClearChannel","WriteOnClearChannel","WriteOnClearChannel method [windows Media Device Manager]","WriteOnClearChannel method [windows Media Device Manager]","IMDSPObject2 interface","mswmdm/IMDSPObject2::WriteOnClearChannel","wmdm.imdspobject2_writeonclearchannel"]
old-location: wmdm\imdspobject2_writeonclearchannel.htm
tech.root: WMDM
ms.assetid: 9c80f382-2536-4f08-9111-94ad757747f7
ms.date: 12/05/2018
ms.keywords: IMDSPObject2 interface [windows Media Device Manager],WriteOnClearChannel method, IMDSPObject2.WriteOnClearChannel, IMDSPObject2::WriteOnClearChannel, IMDSPObject2WriteOnClearChannel, WriteOnClearChannel, WriteOnClearChannel method [windows Media Device Manager], WriteOnClearChannel method [windows Media Device Manager],IMDSPObject2 interface, mswmdm/IMDSPObject2::WriteOnClearChannel, wmdm.imdspobject2_writeonclearchannel
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
 - IMDSPObject2::WriteOnClearChannel
 - mswmdm/IMDSPObject2::WriteOnClearChannel
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
 - IMDSPObject2.WriteOnClearChannel
---

# IMDSPObject2::WriteOnClearChannel


## -description

The <b>WriteOnClearChannel</b> method writes data to the object to the current position within the object, without using secure authenticated channels. This operation is valid only if the storage object represents a file. If <b>IMDSPObject2</b> is supported, this method must be implemented. Windows Media Device Manager does not fall back to <a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write">IMDSPObject::Write</a> if this method fails.

## -parameters

### -param pData [in]

Pointer to the buffer containing the data to write to the object.

### -param pdwSize [in, out]

Pointer to a <b>DWORD</b> containing the number of bytes of data to write. Upon return, this parameter contains the actual number of bytes written.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

This method can be used with DRM-protected content. It is more efficient than <a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write">IMDSPObject::Write</a> because this method does not involve encrypting and decrypting parameters.

Unlike <b>IMDSPObject::Write</b>, this method does not need to decrypt the data before writing to a device, and is therefore more efficient.

## -see-also

<a href="/windows/desktop/WMDM/enabling-synchronization-with-windows-media-player">Enabling Synchronization with Windows Media Player</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2">IMDSPObject2 Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-readonclearchannel">IMDSPObject2::ReadOnClearChannel</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write">IMDSPObject::Write</a>