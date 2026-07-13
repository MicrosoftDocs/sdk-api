---
UID: NF:txlogpub.IFileBasedLogInit.InitNew
title: IFileBasedLogInit::InitNew (txlogpub.h)
description: Create a new log instance on the specified file. If a file with that name already exists, it is overwritten.
helpviewer_keywords: ["IFileBasedLogInit interface [COM]","InitNew method","IFileBasedLogInit.InitNew","IFileBasedLogInit::InitNew","InitNew","InitNew method [COM]","InitNew method [COM]","IFileBasedLogInit interface","_com_ifilebasedloginit_initnew","com.ifilebasedloginit_initnew","txlogpub/IFileBasedLogInit::InitNew"]
old-location: com\ifilebasedloginit_initnew.htm
tech.root: com
ms.assetid: 729c0cfc-4246-4185-af06-ed90a1955b03
ms.date: 12/05/2018
ms.keywords: IFileBasedLogInit interface [COM],InitNew method, IFileBasedLogInit.InitNew, IFileBasedLogInit::InitNew, InitNew, InitNew method [COM], InitNew method [COM],IFileBasedLogInit interface, _com_ifilebasedloginit_initnew, com.ifilebasedloginit_initnew, txlogpub/IFileBasedLogInit::InitNew
req.header: txlogpub.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Txlogpub.idl
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
 - IFileBasedLogInit::InitNew
 - txlogpub/IFileBasedLogInit::InitNew
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Txlogpub.h
api_name:
 - IFileBasedLogInit.InitNew
---

# IFileBasedLogInit::InitNew


## -description

Create a new log instance on the specified file. If a file with that name already exists, it is overwritten.

## -parameters

### -param filename [in]

The absolute path of the file to be created.

### -param cbCapacityHint [in]

A hint to the implementation about the total capacity that will be needed.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/txlogpub/nn-txlogpub-ifilebasedloginit">IFileBasedLogInit</a>