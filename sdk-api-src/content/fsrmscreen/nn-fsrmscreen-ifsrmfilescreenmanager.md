---
UID: NN:fsrmscreen.IFsrmFileScreenManager
title: IFsrmFileScreenManager (fsrmscreen.h)
description: Used to manage file screen objects.
old-location: fsrm\ifsrmfilescreenmanager.htm
tech.root: fsrm
ms.assetid: a0cea95d-5839-41a2-91b9-da8e13030682
ms.date: 12/05/2018
ms.keywords: IFsrmFileScreenManager, IFsrmFileScreenManager interface [File Server Resource Manager], IFsrmFileScreenManager interface [File Server Resource Manager],described, fs.ifsrmfilescreenmanager, fsrm.ifsrmfilescreenmanager, fsrmscreen/IFsrmFileScreenManager
f1_keywords:
- fsrmscreen/IFsrmFileScreenManager
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
- IFsrmFileScreenManager
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsrmFileScreenManager interface


## -description


Used to manage file screen objects.

To get this interface, call the 
    <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex">CoCreateInstanceEx</a> function. Use 
    <b>CLSID_FsrmFileScreenManager</b> as the class identifier and 
    <code>__uuidof(IFsrmFileScreenManager)</code> as the interface identifier. 
    For an example, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/defining-a-file-screen">Defining a File Screen</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmFileScreenManager</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFsrmFileScreenManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFsrmFileScreenManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenmanager-createfilescreen">CreateFileScreen</a>
</td>
<td align="left" width="63%">
Creates a file screen object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenmanager-createfilescreencollection">CreateFileScreenCollection</a>
</td>
<td align="left" width="63%">
Creates an empty collection to which you can add file screens.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenmanager-createfilescreenexception">CreateFileScreenException</a>
</td>
<td align="left" width="63%">
Creates a file screen exception object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenmanager-enumfilescreenexceptions">EnumFileScreenExceptions</a>
</td>
<td align="left" width="63%">
Enumerates the file screen exceptions for the specified directory and its subdirectories.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenmanager-enumfilescreens">EnumFileScreens</a>
</td>
<td align="left" width="63%">
Enumerates the file screens for the specified directory and its subdirectories.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenmanager-getfilescreen">GetFileScreen</a>
</td>
<td align="left" width="63%">
Retrieves the specified file screen.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenmanager-getfilescreenexception">GetFileScreenException</a>
</td>
<td align="left" width="63%">
Retrieves the specified file screen exception.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmFileScreenManager</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenmanager-get_actionvariabledescriptions">ActionVariableDescriptions</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the descriptions for the macros contained in the 
     <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenmanager-get_actionvariables">ActionVariables</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenmanager-get_actionvariables">ActionVariables</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a  list of macros that you can specify in action property values.

</td>
</tr>
</table> 


## -remarks



file screen restricts the types of files that can be stored in a specific directory and its subdirectories. 
    For each file screen, there is a configurable list of blocked file groups that define a set of patterns (that are 
    based on file name) that will be restricted. When a file is created or renamed, the server evaluates whether the 
    file name matches a pattern in any file group configured on a parent portion of the path. If a match is found, the 
    file is blocked and a set of actions are initiated.

In addition to configuring file screens, you can create a file screen exception that defines a list of file 
    groups that are specifically allowed in a specific directory and its subdirectories. Typically, you will configure 
    a file screen exception on a directory that is in the subtree of a directory with a file screen. In this case, the 
    file screen exception list takes precedence when evaluating screening rules; files with names that match the name 
    patterns in the allowed file groups will not be blocked.

You can create a file screen or a file screen template. The template is used to modify properties in bulk by 
    applying the changes to file screens that derive from the file screen template.

To create this object from a script, use the "Fsrm.FsrmFileScreenManager" program 
    identifier.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-interfaces">FSRM Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrmfilescreenmanager">FsrmFileScreenManager</a>
 

 

