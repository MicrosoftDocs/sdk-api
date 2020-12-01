---
UID: NF:mfidl.MFCreatePMPServer
title: MFCreatePMPServer function (mfidl.h)
description: Creates the protected media path (PMP) server object.
helpviewer_keywords: ["2bf5541e-9b7e-4e7a-a868-4956c1f70882","MFCreatePMPServer","MFCreatePMPServer function [Media Foundation]","mf.mfcreatepmpserver","mfidl/MFCreatePMPServer"]
old-location: mf\mfcreatepmpserver.htm
tech.root: mf
ms.assetid: 2bf5541e-9b7e-4e7a-a868-4956c1f70882
ms.date: 12/05/2018
ms.keywords: 2bf5541e-9b7e-4e7a-a868-4956c1f70882, MFCreatePMPServer, MFCreatePMPServer function [Media Foundation], mf.mfcreatepmpserver, mfidl/MFCreatePMPServer
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreatePMPServer
 - mfidl/MFCreatePMPServer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFCreatePMPServer
---

# MFCreatePMPServer function


## -description

Creates the protected media path (PMP) server object.

## -parameters

### -param dwCreationFlags [in]

A member of the <a href="/windows/desktop/api/mfidl/ne-mfidl-mfpmpsession_creation_flags">MFPMPSESSION_CREATION_FLAGS</a> enumeration that specifies how to create the PMP session.

### -param ppPMPServer [out]

Receives a pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver">IMFPMPServer</a> interface. The caller must release the interface.

## -returns

The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.
              

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>