---
UID: NN:fsrmscreen.IFsrmFileGroupManager
title: IFsrmFileGroupManager (fsrmscreen.h)
description: Used to manage file group objects.
old-location: fsrm\ifsrmfilegroupmanager.htm
tech.root: fsrm
ms.assetid: e0a1a3d3-f683-410d-a0d9-081cd2476d1e
ms.date: 12/05/2018
ms.keywords: IFsrmFileGroupManager, IFsrmFileGroupManager interface [File Server Resource Manager], IFsrmFileGroupManager interface [File Server Resource Manager],described, fs.ifsrmfilegroupmanager, fsrm.ifsrmfilegroupmanager, fsrmscreen/IFsrmFileGroupManager
f1_keywords:
- fsrmscreen/IFsrmFileGroupManager
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- SrmSvc.dll
api_name:
- IFsrmFileGroupManager
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsrmFileGroupManager interface


## -description


<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmfilegroup">MSFT_FSRMFileGroup</a> class.]

Used to manage file group objects.

To get this interface, call the 
    <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex">CoCreateInstanceEx</a> function. Use 
    <b>CLSID_FsrmFileGroupManager</b> as the class identifier and 
    <code>__uuidof(IFsrmFileGroupManager)</code> as the interface identifier. For an 
    example, see 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/creating-file-groups-to-specify-the-files-to-restrict">Creating File Groups to Specify the Files to Restrict</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmFileGroupManager</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFsrmFileGroupManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFsrmFileGroupManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilegroupmanager-createfilegroup">CreateFileGroup</a>
</td>
<td align="left" width="63%">
Creates a file group object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilegroupmanager-enumfilegroups">EnumFileGroups</a>
</td>
<td align="left" width="63%">
Enumerates the file groups in FSRM.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilegroupmanager-exportfilegroups">ExportFileGroups</a>
</td>
<td align="left" width="63%">
Exports the specified file groups as an XML string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilegroupmanager-getfilegroup">GetFileGroup</a>
</td>
<td align="left" width="63%">
Retrieves the specified file group from FSRM.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilegroupmanager-importfilegroups">ImportFileGroups</a>
</td>
<td align="left" width="63%">
Imports the specified file groups from an XML string.

</td>
</tr>
</table> 


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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-interfaces">FSRM Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrmfilegroupmanager">FsrmFileGroupManager</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmfilegroup">MSFT_FSRMFileGroup</a>
 

 

