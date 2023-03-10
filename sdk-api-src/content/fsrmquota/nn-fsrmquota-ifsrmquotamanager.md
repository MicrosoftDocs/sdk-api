---
UID: NN:fsrmquota.IFsrmQuotaManager
title: IFsrmQuotaManager (fsrmquota.h)
description: Used to manage quotas.
helpviewer_keywords: ["IFsrmQuotaManager","IFsrmQuotaManager interface [File Server Resource Manager]","IFsrmQuotaManager interface [File Server Resource Manager]","described","fs.ifsrmquotamanager","fsrm.ifsrmquotamanager","fsrmquota/IFsrmQuotaManager"]
old-location: fsrm\ifsrmquotamanager.htm
tech.root: fsrm
ms.assetid: 20bda7d6-5c7b-4066-82e2-83ad52515568
ms.date: 12/05/2018
ms.keywords: IFsrmQuotaManager, IFsrmQuotaManager interface [File Server Resource Manager], IFsrmQuotaManager interface [File Server Resource Manager],described, fs.ifsrmquotamanager, fsrm.ifsrmquotamanager, fsrmquota/IFsrmQuotaManager
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
 - IFsrmQuotaManager
 - fsrmquota/IFsrmQuotaManager
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
 - IFsrmQuotaManager
---

# IFsrmQuotaManager interface


## -description

<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a> class.]

Used to manage quotas.

To get this interface, call the 
    <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex">CoCreateInstanceEx</a> function. Use 
    <b>CLSID_FsrmQuotaManager</b> as the class identifier and 
    <code>__uuidof(IFsrmQuotaManager)</code> as the interface identifier. For 
    an example, see <a href="/previous-versions/windows/desktop/fsrm/defining-a-quota">Defining a Quota</a>.

## -inheritance

The <b>IFsrmQuotaManager</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFsrmQuotaManager</b> also has these types of members:

## -remarks

A directory quota restricts the size of a specific directory to a configurable quota limit. In addition to 
    the limit, a directory quota may be configured with one or more directory quota thresholds which define a set of 
    actions that are initiated when the quota usage reaches the threshold value.

You can create a quota, an automatic quota, or a quota template. A quota applies to a specific directory. The 
    automatic quota applies to the specified directory and automatically creates quotas for new and existing 
    subdirectories of the specified directory. The quota template is used to modify properties in bulk by applying 
    the changes to quotas that derive from the quota template.

Note that if the directory is renamed, the quota applies to the renamed directory. If the directory is 
    deleted, the quota is deleted.

To create this object from a script, use the program identifier, 
    "Fsrm.FsrmQuotaManager".

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrm-interfaces">FSRM Interfaces</a>



<a href="/previous-versions/windows/desktop/fsrm/fsrmquotamanager">FsrmQuotaManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotamanagerex">IFsrmQuotaManagerEx</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a>
