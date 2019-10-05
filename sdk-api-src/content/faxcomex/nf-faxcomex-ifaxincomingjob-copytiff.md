---
UID: NF:faxcomex.IFaxIncomingJob.CopyTiff
title: IFaxIncomingJob::CopyTiff (faxcomex.h)
author: windows-sdk-content
description: The CopyTiff method copies the Tagged Image File Format Class F (TIFF Class F) file associated with the inbound fax job to a file on the local computer.
old-location: fax\_mfax_faxincomingjob_cpp_mfax_faxincomingjob_copytiff_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_136u.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CopyTiff, CopyTiff method [Fax Service], CopyTiff method [Fax Service],IFaxIncomingJob interface, IFaxIncomingJob interface [Fax Service],CopyTiff method, IFaxIncomingJob.CopyTiff, IFaxIncomingJob::CopyTiff, _mfax_faxincomingjob.copytiff, fax._mfax_faxincomingjob_copytiff, fax._mfax_faxincomingjob_cpp_mfax_faxincomingjob_copytiff_cpp, faxcomex/IFaxIncomingJob::CopyTiff
ms.topic: method
f1_keywords: 
 - "faxcomex/IFaxIncomingJob.CopyTiff"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxIncomingJob.CopyTiff
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxIncomingJob::CopyTiff


## -description


The <b>CopyTiff</b> method copies the Tagged Image File Format Class F (TIFF Class F) file associated with the inbound fax job to a file on the local computer.


## -parameters




### -param bstrTiffPath [in]

Type: <b>BSTR</b>

Null-terminated string that specifies a fully qualified path and file name on the local computer.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_JOBS</a> access right.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjob">FaxIncomingJob</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingjob">IFaxIncomingJob</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-managing-the-incoming-queue">Visual Basic Example</a>
 

 

