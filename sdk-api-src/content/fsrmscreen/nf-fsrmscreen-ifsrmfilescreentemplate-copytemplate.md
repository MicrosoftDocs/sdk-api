---
UID: NF:fsrmscreen.IFsrmFileScreenTemplate.CopyTemplate
title: IFsrmFileScreenTemplate::CopyTemplate (fsrmscreen.h)
description: Copies the property values of the specified template to this template. (IFsrmFileScreenTemplate.CopyTemplate)
helpviewer_keywords: ["CopyTemplate","CopyTemplate method [File Server Resource Manager]","CopyTemplate method [File Server Resource Manager]","IFsrmFileScreenTemplate interface","IFsrmFileScreenTemplate interface [File Server Resource Manager]","CopyTemplate method","IFsrmFileScreenTemplate.CopyTemplate","IFsrmFileScreenTemplate::CopyTemplate","fs.ifsrmfilescreentemplate_copytemplate","fsrm.ifsrmfilescreentemplate_copytemplate","fsrmscreen/IFsrmFileScreenTemplate::CopyTemplate"]
old-location: fsrm\ifsrmfilescreentemplate_copytemplate.htm
tech.root: fsrm
ms.assetid: c6c69f15-9a7c-43f4-9d68-a54c333453f5
ms.date: 12/05/2018
ms.keywords: CopyTemplate, CopyTemplate method [File Server Resource Manager], CopyTemplate method [File Server Resource Manager],IFsrmFileScreenTemplate interface, IFsrmFileScreenTemplate interface [File Server Resource Manager],CopyTemplate method, IFsrmFileScreenTemplate.CopyTemplate, IFsrmFileScreenTemplate::CopyTemplate, fs.ifsrmfilescreentemplate_copytemplate, fsrm.ifsrmfilescreentemplate_copytemplate, fsrmscreen/IFsrmFileScreenTemplate::CopyTemplate
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
 - IFsrmFileScreenTemplate::CopyTemplate
 - fsrmscreen/IFsrmFileScreenTemplate::CopyTemplate
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
 - IFsrmFileScreenTemplate.CopyTemplate
---

# IFsrmFileScreenTemplate::CopyTemplate


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilescreentemplate">MSFT_FSRMFileScreenTemplate</a> class.]

Copies the property values of the specified template to this template.

## -parameters

### -param fileScreenTemplateName [in]

The name of another template from which to copy the property values. The name is limited to 4,000 characters.

## -returns

The method returns the following return values.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilescreentemplate">IFsrmFileScreenTemplate</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilescreentemplate">MSFT_FSRMFileScreenTemplate</a>
