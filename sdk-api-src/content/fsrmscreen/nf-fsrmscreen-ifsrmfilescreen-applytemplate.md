---
UID: NF:fsrmscreen.IFsrmFileScreen.ApplyTemplate
title: IFsrmFileScreen::ApplyTemplate (fsrmscreen.h)
description: Applies the property values of the specified file screen template to this file screen object.
helpviewer_keywords: ["ApplyTemplate","ApplyTemplate method [File Server Resource Manager]","ApplyTemplate method [File Server Resource Manager]","IFsrmFileScreen interface","IFsrmFileScreen interface [File Server Resource Manager]","ApplyTemplate method","IFsrmFileScreen.ApplyTemplate","IFsrmFileScreen::ApplyTemplate","fs.ifsrmfilescreen_applytemplate","fsrm.ifsrmfilescreen_applytemplate","fsrmscreen/IFsrmFileScreen::ApplyTemplate"]
old-location: fsrm\ifsrmfilescreen_applytemplate.htm
tech.root: fsrm
ms.assetid: d495cb92-09c4-4fa5-873c-5f07475eb7bf
ms.date: 12/05/2018
ms.keywords: ApplyTemplate, ApplyTemplate method [File Server Resource Manager], ApplyTemplate method [File Server Resource Manager],IFsrmFileScreen interface, IFsrmFileScreen interface [File Server Resource Manager],ApplyTemplate method, IFsrmFileScreen.ApplyTemplate, IFsrmFileScreen::ApplyTemplate, fs.ifsrmfilescreen_applytemplate, fsrm.ifsrmfilescreen_applytemplate, fsrmscreen/IFsrmFileScreen::ApplyTemplate
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
 - IFsrmFileScreen::ApplyTemplate
 - fsrmscreen/IFsrmFileScreen::ApplyTemplate
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
 - IFsrmFileScreen.ApplyTemplate
---

# IFsrmFileScreen::ApplyTemplate


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilescreen">MSFT_FSRMFileScreen</a> class.]

Applies the property values of the specified file screen template to this file screen 
    object.

## -parameters

### -param fileScreenTemplateName [in]

The name of the file screen template. The string is limited to 4,000 characters.

## -returns

The method returns the following return values.

## -remarks

To save the changes, call the 
    <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmobject-commit">IFsrmFileScreen::Commit</a> method.

The specified template must be a committed template; you cannot apply a newly created template that has not 
    been committed.


#### Examples

For an example, see 
     <a href="/previous-versions/windows/desktop/fsrm/defining-a-file-screen">Defining a File Screen</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilescreen">IFsrmFileScreen</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilescreen">MSFT_FSRMFileScreen</a>