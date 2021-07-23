---
UID: NN:fsrmquota.IFsrmQuotaTemplateManager
title: IFsrmQuotaTemplateManager (fsrmquota.h)
description: Used to manage quota templates.
helpviewer_keywords: ["IFsrmQuotaTemplateManager","IFsrmQuotaTemplateManager interface [File Server Resource Manager]","IFsrmQuotaTemplateManager interface [File Server Resource Manager]","described","fs.ifsrmquotatemplatemanager","fsrm.ifsrmquotatemplatemanager","fsrmquota/IFsrmQuotaTemplateManager"]
old-location: fsrm\ifsrmquotatemplatemanager.htm
tech.root: fsrm
ms.assetid: c6e782ff-b2e7-4bd6-bd9f-cc645c6ee5d6
ms.date: 12/05/2018
ms.keywords: IFsrmQuotaTemplateManager, IFsrmQuotaTemplateManager interface [File Server Resource Manager], IFsrmQuotaTemplateManager interface [File Server Resource Manager],described, fs.ifsrmquotatemplatemanager, fsrm.ifsrmquotatemplatemanager, fsrmquota/IFsrmQuotaTemplateManager
req.header: fsrmquota.h
req.include-header: FsrmQuota.h, FsrmTlb.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IFsrmQuotaTemplateManager
 - fsrmquota/IFsrmQuotaTemplateManager
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
 - IFsrmQuotaTemplateManager
---

# IFsrmQuotaTemplateManager interface


## -description

<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a> class.]

Used to manage quota templates.

To get this interface, call the 
    <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex">CoCreateInstanceEx</a> function. Use 
    <b>CLSID_FsrmQuotaTemplateManager</b> as the class identifier and 
    <code>__uuidof(IFsrmQuotaTemplateManager)</code> as the interface 
    identifier. For an example, see 
    <a href="/previous-versions/windows/desktop/fsrm/using-templates-to-define-quotas">Using Templates to Define Quotas</a>.

## -inheritance

The <b>IFsrmQuotaTemplateManager</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFsrmQuotaTemplateManager</b> also has these types of members:

## -remarks

Note that a new installation of the operating system includes FSRM-defined templates.

To create this object from a script, use the "Fsrm.FsrmQuotaTemplateManager" program 
    identifier.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrm-interfaces">FSRM Interfaces</a>



<a href="/previous-versions/windows/desktop/fsrm/fsrmquotatemplatemanager">FsrmQuotaTemplateManager</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a>
