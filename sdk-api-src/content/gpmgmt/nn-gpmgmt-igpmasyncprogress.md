---
UID: NN:gpmgmt.IGPMAsyncProgress
title: IGPMAsyncProgress (gpmgmt.h)
description: The IGPMAsyncProgress interface can be implemented by the client and passed as an input parameter to the Group Policy Management Console (GPMC) methods that can execute asynchronously.
helpviewer_keywords: ["IGPMAsyncProgress","IGPMAsyncProgress interface [GPMC]","IGPMAsyncProgress interface [GPMC]","described","_win32_igpmasyncprogress","gpmc.igpmasyncprogress","gpmgmt/IGPMAsyncProgress"]
old-location: gpmc\igpmasyncprogress.htm
tech.root: gpmc
ms.assetid: f48b90db-5984-4ea7-826b-6fbbf3c33788
ms.date: 12/05/2018
ms.keywords: IGPMAsyncProgress, IGPMAsyncProgress interface [GPMC], IGPMAsyncProgress interface [GPMC],described, _win32_igpmasyncprogress, gpmc.igpmasyncprogress, gpmgmt/IGPMAsyncProgress
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGPMAsyncProgress
 - gpmgmt/IGPMAsyncProgress
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMAsyncProgress
---

# IGPMAsyncProgress interface


## -description

The <b>IGPMAsyncProgress</b> interface can be implemented by the client and passed as an 
    input parameter to the Group Policy Management Console (GPMC) methods that can execute asynchronously. The server 
    will then notify the client about the progress of the operation. Methods include 
    <a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmgpo-generatereport">IGPMGPO::GenerateReport</a>, 
    <a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmbackup-generatereport">IGPMBackup::GenerateReport</a>, 
    <a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmrsop-generatereport">IGPMRSOP::GenerateReport</a>, 
    <a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmdomain-restoregpo">RestoreGPO</a>, 
    <a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmgpo-backup">Backup</a>, 
    <a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmgpo-import">Import</a>, and 
    <a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmgpo-copyto">CopyTo</a>. This object cannot be accessed through scripting. 
    For more information, see the "Remarks" section.

## -inheritance

The <b>IGPMAsyncProgress</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IGPMAsyncProgress</b> also has these types of members:

## -remarks

Complex GPMC operations, such as backup, restore, import, and copy operations, can execute asynchronously. To 
    use this interface with asynchronous operations, follow these steps.

<p class="proch"><b>To use this interface with asynchronous operations</b>

<ol>
<li>Implement the <b>IGPMAsyncProgress</b> interface.</li>
<li>Pass the <b>IGPMAsyncProgress</b> interface pointer to the GPMC method. For example, 
      pass the interface pointer to the 
      <a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmdomain-restoregpo">RestoreGPO</a> method or to the 
      <a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmgpo-import">Import</a> method.</li>
</ol>
The server will call the <a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmasyncprogress-status">Status</a> method to 
    notify the client about the progress of the operation. This method also returns an 
    <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmasynccancel">IGPMAsyncCancel</a> interface pointer so that the caller can cancel the 
    operation by calling the <a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmasynccancel-cancel">Cancel</a> method.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmasynccancel">IGPMAsyncCancel</a>
