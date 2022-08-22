---
UID: NF:fsrmscreen.IFsrmFileScreenTemplate.get_Name
title: IFsrmFileScreenTemplate::get_Name (fsrmscreen.h)
description: Retrieves and sets the name of the file screen template. (Get)
helpviewer_keywords: ["IFsrmFileScreenTemplate interface [File Server Resource Manager]","Name property","IFsrmFileScreenTemplate.Name","IFsrmFileScreenTemplate.get_Name","IFsrmFileScreenTemplate::Name","IFsrmFileScreenTemplate::get_Name","IFsrmFileScreenTemplate::put_Name","Name property [File Server Resource Manager]","Name property [File Server Resource Manager]","IFsrmFileScreenTemplate interface","fs.ifsrmfilescreentemplate_name","fsrm.ifsrmfilescreentemplate_name","fsrmscreen/IFsrmFileScreenTemplate::Name","fsrmscreen/IFsrmFileScreenTemplate::get_Name","fsrmscreen/IFsrmFileScreenTemplate::put_Name","get_Name"]
old-location: fsrm\ifsrmfilescreentemplate_name.htm
tech.root: fsrm
ms.assetid: b72309d1-8b8e-46bc-bca4-e6e47dae88e8
ms.date: 12/05/2018
ms.keywords: IFsrmFileScreenTemplate interface [File Server Resource Manager],Name property, IFsrmFileScreenTemplate.Name, IFsrmFileScreenTemplate.get_Name, IFsrmFileScreenTemplate::Name, IFsrmFileScreenTemplate::get_Name, IFsrmFileScreenTemplate::put_Name, Name property [File Server Resource Manager], Name property [File Server Resource Manager],IFsrmFileScreenTemplate interface, fs.ifsrmfilescreentemplate_name, fsrm.ifsrmfilescreentemplate_name, fsrmscreen/IFsrmFileScreenTemplate::Name, fsrmscreen/IFsrmFileScreenTemplate::get_Name, fsrmscreen/IFsrmFileScreenTemplate::put_Name, get_Name
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
 - IFsrmFileScreenTemplate::get_Name
 - fsrmscreen/IFsrmFileScreenTemplate::get_Name
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
 - IFsrmFileScreenTemplate.Name
 - IFsrmFileScreenTemplate.get_Name
 - IFsrmFileScreenTemplate.put_Name
---

# IFsrmFileScreenTemplate::get_Name


## -description

<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilescreentemplate">MSFT_FSRMFileScreenTemplate</a> class.]

Retrieves and sets the name of the file screen template.

This property is read/write.

## -parameters

## -remarks

If a template with the specified name exists, the template fails with 
    <b>FSRM_E_ALREADY_EXISTS</b> when you call the 
    <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmobject-commit">IFsrmFileScreen::Commit</a> method.


#### Examples

For an example, see 
     <a href="/previous-versions/windows/desktop/fsrm/using-templates-to-define-file-screens">Using Templates to Define File Screens</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilescreentemplate">IFsrmFileScreenTemplate</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilescreentemplate">MSFT_FSRMFileScreenTemplate</a>
