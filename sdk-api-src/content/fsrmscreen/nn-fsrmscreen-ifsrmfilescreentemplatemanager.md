---
UID: NN:fsrmscreen.IFsrmFileScreenTemplateManager
title: IFsrmFileScreenTemplateManager
author: windows-sdk-content
description: Used to manage file screen templates.
old-location: fsrm\ifsrmfilescreentemplatemanager.htm
old-project: Fsrm
ms.assetid: 89577ab3-2648-4b37-9fc0-c64929223a13
ms.author: windowssdkdev
ms.date: 04/18/2018
ms.keywords: IFsrmFileScreenTemplateManager, IFsrmFileScreenTemplateManager interface [File Server Resource Manager], IFsrmFileScreenTemplateManager interface [File Server Resource Manager],described, fs.ifsrmfilescreentemplatemanager, fsrm.ifsrmfilescreentemplatemanager, fsrmscreen/IFsrmFileScreenTemplateManager
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: FsrmTemplateApplyOptions
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SrmSvc.dll
api_name:
-	IFsrmFileScreenTemplateManager
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmFileScreenTemplateManager interface


## -description


Used to manage file screen templates.

To get this interface, call the 
    <a href="_com_CoCreateInstanceEx">CoCreateInstanceEx</a> function. Use 
    <b>CLSID_FsrmFileScreenTemplateManager</b> as the class identifier and 
    <code>__uuidof(IFsrmFileScreenTemplateManager)</code> as the interface 
    identifier. For an example, see 
    <a href="https://msdn.microsoft.com/c76c0cc5-1109-46ec-be4d-c6c5f14a6df7">Using Templates to Define File Screens</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmFileScreenTemplateManager</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFsrmFileScreenTemplateManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFsrmFileScreenTemplateManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3d654dee-2a27-4dc0-8e2b-fba546abe17e">CreateTemplate</a>
</td>
<td align="left" width="63%">
Creates a file screen template object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5bfb82f9-50a5-4266-956d-f99e2982a6a5">EnumTemplates</a>
</td>
<td align="left" width="63%">
Enumerates the file screen templates on the server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/27a0141d-0906-400e-bd5f-81da67a3c501">ExportTemplates</a>
</td>
<td align="left" width="63%">
Exports the file screen templates as an XML string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e97149f6-8cf5-433c-a487-799322253e44">GetTemplate</a>
</td>
<td align="left" width="63%">
Retrieves the specified file screen template.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0660a1cb-904e-4ed0-bbc8-9903e8848f4e">ImportTemplates</a>
</td>
<td align="left" width="63%">
Imports the specified file screen templates from an XML string.

</td>
</tr>
</table> 


## -remarks



Note that a new installation of the operating system includes FSRM-defined templates.

To create this object from a script, use the "Fsrm.FsrmFileScreenTemplateManager" program 
    identifier.




## -see-also




<a href="https://msdn.microsoft.com/bbd888d9-1005-4173-8e82-ced13e68c09e">FSRM Interfaces</a>



<a href="https://msdn.microsoft.com/e736def1-ebfd-4f3e-9729-f8dd46f59516">FsrmFileScreenTemplateManager</a>
 

 

