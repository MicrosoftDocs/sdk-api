---
UID: NN:fsrmscreen.IFsrmFileGroupManager
title: IFsrmFileGroupManager
author: windows-driver-content
description: Used to manage file group objects.
old-location: fsrm\ifsrmfilegroupmanager.htm
old-project: Fsrm
ms.assetid: e0a1a3d3-f683-410d-a0d9-081cd2476d1e
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: IFsrmFileGroupManager, IFsrmFileGroupManager interface [File Server Resource Manager], IFsrmFileGroupManager interface [File Server Resource Manager],described, fs.ifsrmfilegroupmanager, fsrm.ifsrmfilegroupmanager, fsrmscreen/IFsrmFileGroupManager
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: FsrmTemplateApplyOptions
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SrmSvc.dll
api_name:
-	IFsrmFileGroupManager
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmFileGroupManager interface


## -description


<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/c090da1e-df74-4dba-aaa0-15defa85d604">MSFT_FSRMFileGroup</a> class.]

Used to manage file group objects.

To get this interface, call the 
    <a href="_com_CoCreateInstanceEx">CoCreateInstanceEx</a> function. Use 
    <b>CLSID_FsrmFileGroupManager</b> as the class identifier and 
    <code>__uuidof(IFsrmFileGroupManager)</code> as the interface identifier. For an 
    example, see 
    <a href="https://msdn.microsoft.com/951f5757-28fb-4583-9850-a11f60df05f5">Creating File Groups to Specify the Files to Restrict</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmFileGroupManager</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFsrmFileGroupManager</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/7e2c3672-fbb9-4da5-9e20-25c66213843c">CreateFileGroup</a>
</td>
<td align="left" width="63%">
Creates a file group object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/317eb6cf-7bcc-4042-a7b7-05efac84a0c2">EnumFileGroups</a>
</td>
<td align="left" width="63%">
Enumerates the file groups in FSRM.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59d7ef32-f06b-4167-8e28-da88da27ab0a">ExportFileGroups</a>
</td>
<td align="left" width="63%">
Exports the specified file groups as an XML string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14b61b2b-a20e-4895-bfbe-40e9dfe0c496">GetFileGroup</a>
</td>
<td align="left" width="63%">
Retrieves the specified file group from FSRM.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/81f62d49-5fce-4d8c-96b5-506d741c5f77">ImportFileGroups</a>
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




<a href="https://msdn.microsoft.com/bbd888d9-1005-4173-8e82-ced13e68c09e">FSRM Interfaces</a>



<a href="https://msdn.microsoft.com/d5c9c8f0-edbe-4f34-8f34-fe9d0667926e">FsrmFileGroupManager</a>



<a href="https://msdn.microsoft.com/c090da1e-df74-4dba-aaa0-15defa85d604">MSFT_FSRMFileGroup</a>
 

 

