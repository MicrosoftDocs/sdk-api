---
UID: NN:fsrmscreen.IFsrmFileScreen
title: IFsrmFileScreen (fsrmscreen.h)
description: Used to configure a file screen that blocks groups of files from being saved to the specified directory.
helpviewer_keywords: ["IFsrmFileScreen","IFsrmFileScreen interface [File Server Resource Manager]","IFsrmFileScreen interface [File Server Resource Manager]","described","fs.ifsrmfilescreen","fsrm.ifsrmfilescreen","fsrmscreen/IFsrmFileScreen"]
old-location: fsrm\ifsrmfilescreen.htm
tech.root: fsrm
ms.assetid: 69b831a1-c935-4de0-b222-009bafc45ec5
ms.date: 12/05/2018
ms.keywords: IFsrmFileScreen, IFsrmFileScreen interface [File Server Resource Manager], IFsrmFileScreen interface [File Server Resource Manager],described, fs.ifsrmfilescreen, fsrm.ifsrmfilescreen, fsrmscreen/IFsrmFileScreen
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
 - IFsrmFileScreen
 - fsrmscreen/IFsrmFileScreen
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
 - IFsrmFileScreen
---

# IFsrmFileScreen interface


## -description

<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilescreen">MSFT_FSRMFileScreen</a> class.]

Used to configure a file screen that blocks groups of files from being saved to the specified 
    directory.

To create this interface, call the 
    <a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenmanager-createfilescreen">IFsrmFileScreenManager::CreateFileScreen</a> 
    method.

The following methods return this interface:
<ul>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenmanager-enumfilescreens">IFsrmFileScreenManager::EnumFileScreens</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenmanager-getfilescreen">IFsrmFileScreenManager::GetFileScreen</a>
</li>
</ul>

## -inheritance

The <b>IFsrmFileScreen</b> interface inherits from <a href="/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilescreenbase">IFsrmFileScreenBase</a>. <b>IFsrmFileScreen</b> also has these types of members:

## -remarks

A file screen limits the types of files that the system or any user can store in a directory. When a 
    restricted file is detected, the FSRM server performs the specified actions (see 
    <a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenbase-createaction">IFsrmFileScreenBase::CreateAction</a>).

The file screen applies to future files—the screen is not applied retroactively. To list 
    the files in the directory that violate the screen, create a report job that lists files by type.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilescreenbase">IFsrmFileScreenBase</a>



<a href="/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilescreenexception">IFsrmFileScreenException</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilescreen">MSFT_FSRMFileScreen</a>
