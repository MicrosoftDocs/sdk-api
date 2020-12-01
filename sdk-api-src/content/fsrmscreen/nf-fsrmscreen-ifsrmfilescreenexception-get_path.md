---
UID: NF:fsrmscreen.IFsrmFileScreenException.get_Path
title: IFsrmFileScreenException::get_Path (fsrmscreen.h)
description: Retrieves the path that is associated with this file screen exception.
helpviewer_keywords: ["IFsrmFileScreenException interface [File Server Resource Manager]","Path property","IFsrmFileScreenException.Path","IFsrmFileScreenException.get_Path","IFsrmFileScreenException::Path","IFsrmFileScreenException::get_Path","Path property [File Server Resource Manager]","Path property [File Server Resource Manager]","IFsrmFileScreenException interface","fs.ifsrmfilescreenexception_path","fsrm.ifsrmfilescreenexception_path","fsrmscreen/IFsrmFileScreenException::Path","fsrmscreen/IFsrmFileScreenException::get_Path","get_Path"]
old-location: fsrm\ifsrmfilescreenexception_path.htm
tech.root: fsrm
ms.assetid: ac447042-b87b-4387-bb8f-2e69df9e7f8f
ms.date: 12/05/2018
ms.keywords: IFsrmFileScreenException interface [File Server Resource Manager],Path property, IFsrmFileScreenException.Path, IFsrmFileScreenException.get_Path, IFsrmFileScreenException::Path, IFsrmFileScreenException::get_Path, Path property [File Server Resource Manager], Path property [File Server Resource Manager],IFsrmFileScreenException interface, fs.ifsrmfilescreenexception_path, fsrm.ifsrmfilescreenexception_path, fsrmscreen/IFsrmFileScreenException::Path, fsrmscreen/IFsrmFileScreenException::get_Path, get_Path
req.header: fsrmscreen.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FsrmScreen.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsrmFileScreenException::get_Path
 - fsrmscreen/IFsrmFileScreenException::get_Path
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmFileScreenException.Path
 - IFsrmFileScreenException.get_Path
---

# IFsrmFileScreenException::get_Path


## -description

<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilescreenexception">MSFT_FSRMFileScreenException</a> class.]

Retrieves the path that is associated with this file screen exception.

This property is read-only.

## -parameters

## -remarks

Note that if the path is renamed, the exception becomes associated with the new path. If the path is deleted, 
    the exception is deleted.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilescreenexception">IFsrmFileScreenException</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilescreenexception">MSFT_FSRMFileScreenException</a>