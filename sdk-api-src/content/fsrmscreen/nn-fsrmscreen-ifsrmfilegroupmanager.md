---
UID: NN:fsrmscreen.IFsrmFileGroupManager
title: IFsrmFileGroupManager (fsrmscreen.h)
description: Used to manage file group objects.
helpviewer_keywords: ["IFsrmFileGroupManager","IFsrmFileGroupManager interface [File Server Resource Manager]","IFsrmFileGroupManager interface [File Server Resource Manager]","described","fs.ifsrmfilegroupmanager","fsrm.ifsrmfilegroupmanager","fsrmscreen/IFsrmFileGroupManager"]
old-location: fsrm\ifsrmfilegroupmanager.htm
tech.root: fsrm
ms.assetid: e0a1a3d3-f683-410d-a0d9-081cd2476d1e
ms.date: 12/05/2018
ms.keywords: IFsrmFileGroupManager, IFsrmFileGroupManager interface [File Server Resource Manager], IFsrmFileGroupManager interface [File Server Resource Manager],described, fs.ifsrmfilegroupmanager, fsrm.ifsrmfilegroupmanager, fsrmscreen/IFsrmFileGroupManager
req.header: fsrmscreen.h
req.include-header: FsrmScreen.h, FsrmTlb.h
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
 - IFsrmFileGroupManager
 - fsrmscreen/IFsrmFileGroupManager
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
 - IFsrmFileGroupManager
---

# IFsrmFileGroupManager interface


## -description

<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilegroup">MSFT_FSRMFileGroup</a> class.]

Used to manage file group objects.

To get this interface, call the 
    <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex">CoCreateInstanceEx</a> function. Use 
    <b>CLSID_FsrmFileGroupManager</b> as the class identifier and 
    <code>__uuidof(IFsrmFileGroupManager)</code> as the interface identifier. For an 
    example, see 
    <a href="/previous-versions/windows/desktop/fsrm/creating-file-groups-to-specify-the-files-to-restrict">Creating File Groups to Specify the Files to Restrict</a>.

## -inheritance

The <b>IFsrmFileGroupManager</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFsrmFileGroupManager</b> also has these types of members:

## -remarks

FSRM defines the following groups:

<ul>
<li>Audio and Video Files</li>
<li>Backup Files</li>
<li>Compressed Files</li>
<li>Email Files</li>
<li>Executable Files</li>
<li>Image Files</li>
<li>Office Files</li>
<li>System Files</li>
<li>Temporary Files</li>
<li>Text Files</li>
<li>Webpage Files</li>
</ul>
To create this object from a script, use the "Fsrm.FsrmFileGroupManager" program 
    identifier.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrm-interfaces">FSRM Interfaces</a>



<a href="/previous-versions/windows/desktop/fsrm/fsrmfilegroupmanager">FsrmFileGroupManager</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilegroup">MSFT_FSRMFileGroup</a>
