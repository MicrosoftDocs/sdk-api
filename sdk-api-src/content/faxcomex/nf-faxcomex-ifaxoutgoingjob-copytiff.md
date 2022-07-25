---
UID: NF:faxcomex.IFaxOutgoingJob.CopyTiff
title: IFaxOutgoingJob::CopyTiff (faxcomex.h)
description: The IFaxOutgoingJob::CopyTiff method copies the Tagged Image File Format Class F (TIFF Class F) file associated with the outbound fax job, to a file on the local computer.
helpviewer_keywords: ["CopyTiff","CopyTiff method [Fax Service]","CopyTiff method [Fax Service]","IFaxOutgoingJob interface","IFaxOutgoingJob interface [Fax Service]","CopyTiff method","IFaxOutgoingJob.CopyTiff","IFaxOutgoingJob::CopyTiff","_mfax_faxoutgoingjob.copytiff","fax._mfax_faxoutgoingjob_copytiff","fax._mfax_faxoutgoingjob_cpp_mfax_faxoutgoingjob_copytiff_cpp","faxcomex/IFaxOutgoingJob::CopyTiff"]
old-location: fax\_mfax_faxoutgoingjob_cpp_mfax_faxoutgoingjob_copytiff_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_8mli.htm
ms.date: 12/05/2018
ms.keywords: CopyTiff, CopyTiff method [Fax Service], CopyTiff method [Fax Service],IFaxOutgoingJob interface, IFaxOutgoingJob interface [Fax Service],CopyTiff method, IFaxOutgoingJob.CopyTiff, IFaxOutgoingJob::CopyTiff, _mfax_faxoutgoingjob.copytiff, fax._mfax_faxoutgoingjob_copytiff, fax._mfax_faxoutgoingjob_cpp_mfax_faxoutgoingjob_copytiff_cpp, faxcomex/IFaxOutgoingJob::CopyTiff
req.header: faxcomex.h
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
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxOutgoingJob::CopyTiff
 - faxcomex/IFaxOutgoingJob::CopyTiff
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxOutgoingJob.CopyTiff
---

# IFaxOutgoingJob::CopyTiff


## -description

The <b>IFaxOutgoingJob::CopyTiff</b> method copies the Tagged Image File Format Class F (TIFF Class F) file associated with the outbound fax job, to a file on the local computer.

## -parameters

### -param bstrTiffPath

Type: <b>BSTR</b>

Null-terminated string that contains a fully qualified path and file name on the local computer. The fax service will copy the TIFF Class F file associated with the outbound fax to the specified file.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farSUBMIT_LOW</a> or <b>farQUERY_JOBS</b> access right.

With the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farSUBMIT_LOW</a> access right, users will be able to use this method only for their own faxes. With the <b>farQUERY_JOBS</b> access right, users will be able to use this method for all faxes on the server.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob">FaxOutgoingJob</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingjob">IFaxOutgoingJob</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-outgoing-jobs">Visual Basic Example</a>