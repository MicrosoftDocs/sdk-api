---
UID: NF:fsrmscreen.IFsrmFileScreen.get_Path
title: IFsrmFileScreen::get_Path (fsrmscreen.h)
description: Retrieves the directory path associated with the file screen object.
helpviewer_keywords: ["IFsrmFileScreen interface [File Server Resource Manager]","Path property","IFsrmFileScreen.Path","IFsrmFileScreen.get_Path","IFsrmFileScreen::Path","IFsrmFileScreen::get_Path","Path property [File Server Resource Manager]","Path property [File Server Resource Manager]","IFsrmFileScreen interface","fs.ifsrmfilescreen_path","fsrm.ifsrmfilescreen_path","fsrmscreen/IFsrmFileScreen::Path","fsrmscreen/IFsrmFileScreen::get_Path","get_Path"]
old-location: fsrm\ifsrmfilescreen_path.htm
tech.root: fsrm
ms.assetid: 383e829c-5089-4404-a6bd-429812069e85
ms.date: 12/05/2018
ms.keywords: IFsrmFileScreen interface [File Server Resource Manager],Path property, IFsrmFileScreen.Path, IFsrmFileScreen.get_Path, IFsrmFileScreen::Path, IFsrmFileScreen::get_Path, Path property [File Server Resource Manager], Path property [File Server Resource Manager],IFsrmFileScreen interface, fs.ifsrmfilescreen_path, fsrm.ifsrmfilescreen_path, fsrmscreen/IFsrmFileScreen::Path, fsrmscreen/IFsrmFileScreen::get_Path, get_Path
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
 - IFsrmFileScreen::get_Path
 - fsrmscreen/IFsrmFileScreen::get_Path
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
 - IFsrmFileScreen.Path
 - IFsrmFileScreen.get_Path
---

# IFsrmFileScreen::get_Path


## -description

<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilescreen">MSFT_FSRMFileScreen</a> class.]

Retrieves the directory path associated with the file screen object.

This property is read-only.

## -parameters

## -remarks

Note that the file screen remains associated with the directory if the directory is renamed. If the directory 
    is deleted, so is the file screen.


#### Examples

For an example, see 
     <a href="/previous-versions/windows/desktop/fsrm/updating-a-file-screen">Updating a File Screen</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilescreen">IFsrmFileScreen</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilescreen">MSFT_FSRMFileScreen</a>