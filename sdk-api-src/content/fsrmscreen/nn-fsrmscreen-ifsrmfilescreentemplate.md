---
UID: NN:fsrmscreen.IFsrmFileScreenTemplate
title: IFsrmFileScreenTemplate (fsrmscreen.h)
description: Used to configure templates from which new file screens can be derived.
helpviewer_keywords: ["IFsrmFileScreenTemplate","IFsrmFileScreenTemplate interface [File Server Resource Manager]","IFsrmFileScreenTemplate interface [File Server Resource Manager]","described","fs.ifsrmfilescreentemplate","fsrm.ifsrmfilescreentemplate","fsrmscreen/IFsrmFileScreenTemplate"]
old-location: fsrm\ifsrmfilescreentemplate.htm
tech.root: fsrm
ms.assetid: c8e612f5-e7cd-45ff-9eaf-9d1674231161
ms.date: 12/05/2018
ms.keywords: IFsrmFileScreenTemplate, IFsrmFileScreenTemplate interface [File Server Resource Manager], IFsrmFileScreenTemplate interface [File Server Resource Manager],described, fs.ifsrmfilescreentemplate, fsrm.ifsrmfilescreentemplate, fsrmscreen/IFsrmFileScreenTemplate
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
 - IFsrmFileScreenTemplate
 - fsrmscreen/IFsrmFileScreenTemplate
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
 - IFsrmFileScreenTemplate
---

# IFsrmFileScreenTemplate interface


## -description

<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilescreentemplate">MSFT_FSRMFileScreenTemplate</a> class.]

Used to configure templates from which new file screens can be derived. Templates are 
    identified by a name and are used to simplify configuration of file screens.

To create this interface, call the 
    <a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreentemplatemanager-createtemplate">IFsrmFileScreenTemplate::CreateTemplate</a> 
    method.

The following methods return this interface:
<ul>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreentemplatemanager-enumtemplates">IFsrmFileScreenTemplate::EnumTemplates</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreentemplatemanager-gettemplate">IFsrmFileScreenTemplate::GetTemplate</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreentemplatemanager-importtemplates">IFsrmFileScreenTemplate::ImportTemplates</a>
</li>
</ul>

## -inheritance

The <b>IFsrmFileScreenTemplate</b> interface inherits from <a href="/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilescreenbase">IFsrmFileScreenBase</a>. <b>IFsrmFileScreenTemplate</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrm-interfaces">FSRM Interfaces</a>



<a href="/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilescreenbase">IFsrmFileScreenBase</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilescreentemplate">MSFT_FSRMFileScreenTemplate</a>
