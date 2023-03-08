---
UID: NN:imapi2fs.IFsiNamedStreams
title: IFsiNamedStreams (imapi2fs.h)
description: Use this interface to enumerate the named streams associated with a file in a file system image.
helpviewer_keywords: ["IFsiNamedStreams","IFsiNamedStreams interface [IMAPI]","IFsiNamedStreams interface [IMAPI]","described","imapi.ifsinamedstreams","imapi2fs/IFsiNamedStreams"]
old-location: imapi\ifsinamedstreams.htm
tech.root: imapi
ms.assetid: 383a83e4-5dc2-459a-a58f-b6ce7a656348
ms.date: 12/05/2018
ms.keywords: IFsiNamedStreams, IFsiNamedStreams interface [IMAPI], IFsiNamedStreams interface [IMAPI],described, imapi.ifsinamedstreams, imapi2fs/IFsiNamedStreams
req.header: imapi2fs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsiNamedStreams
 - imapi2fs/IFsiNamedStreams
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2fs.h
api_name:
 - IFsiNamedStreams
---

# IFsiNamedStreams interface


## -description

Use this interface to enumerate the named streams associated with a file in a file system image.

## -inheritance

The <b>IFsiNamedStreams</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFsiNamedStreams</b> also has these types of members:

## -remarks

To access this interface, call the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsifileitem2-get_fsinamedstreams">IFsiFileItem2::get_FsiNamedStreams</a> method of a file item object representing a standard or 'Real-Time' file.

This interface is provided only for file item objects representing regular or 'Real-Time' files. Named streams cannot have other name streams associated with them.

UDF must be enabled and set to UDF revision 2.00 or later in order to enable named stream support.

This interface is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.

## -see-also

<b></b>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem2">IFsiFileItem2</a>
