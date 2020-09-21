---
UID: NN:fsrmscreen.IFsrmFileScreenException
title: IFsrmFileScreenException (fsrmscreen.h)
description: Used to configure an exception that excludes the specified files from the file screening process.
helpviewer_keywords: ["IFsrmFileScreenException","IFsrmFileScreenException interface [File Server Resource Manager]","IFsrmFileScreenException interface [File Server Resource Manager]","described","fs.ifsrmfilescreenexception","fsrm.ifsrmfilescreenexception","fsrmscreen/IFsrmFileScreenException"]
old-location: fsrm\ifsrmfilescreenexception.htm
tech.root: fsrm
ms.assetid: 188e76dd-6df6-412f-8d51-fc727075de80
ms.date: 12/05/2018
ms.keywords: IFsrmFileScreenException, IFsrmFileScreenException interface [File Server Resource Manager], IFsrmFileScreenException interface [File Server Resource Manager],described, fs.ifsrmfilescreenexception, fsrm.ifsrmfilescreenexception, fsrmscreen/IFsrmFileScreenException
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
 - IFsrmFileScreenException
 - fsrmscreen/IFsrmFileScreenException
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
 - IFsrmFileScreenException
---

# IFsrmFileScreenException interface


## -description

<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilescreenexception">MSFT_FSRMFileScreenException</a> class.]

Used to configure an exception that excludes the specified files from the file screening 
    process. This allows the  files of a file group to be saved in the directory when a file screen that 
    applies to the directory would otherwise prevent the file from being saved in the directory.

To create this interface, call the 
    <a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenmanager-createfilescreenexception">IFsrmFileScreenManager::CreateFileScreenException</a> 
    method.

The following methods return this interface:
<ul>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenmanager-enumfilescreenexceptions">IFsrmFileScreenManager::EnumFileScreenExceptions</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenmanager-getfilescreenexception">IFsrmFileScreenManager::GetFileScreenException</a>
</li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrm-interfaces">FSRM Interfaces</a>



<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmobject">IFsrmObject</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilescreenexception">MSFT_FSRMFileScreenException</a>