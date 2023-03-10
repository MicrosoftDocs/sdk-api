---
UID: NN:fsrmscreen.IFsrmFileScreenManager
title: IFsrmFileScreenManager (fsrmscreen.h)
description: Used to manage file screen objects.
helpviewer_keywords: ["IFsrmFileScreenManager","IFsrmFileScreenManager interface [File Server Resource Manager]","IFsrmFileScreenManager interface [File Server Resource Manager]","described","fs.ifsrmfilescreenmanager","fsrm.ifsrmfilescreenmanager","fsrmscreen/IFsrmFileScreenManager"]
old-location: fsrm\ifsrmfilescreenmanager.htm
tech.root: fsrm
ms.assetid: a0cea95d-5839-41a2-91b9-da8e13030682
ms.date: 12/05/2018
ms.keywords: IFsrmFileScreenManager, IFsrmFileScreenManager interface [File Server Resource Manager], IFsrmFileScreenManager interface [File Server Resource Manager],described, fs.ifsrmfilescreenmanager, fsrm.ifsrmfilescreenmanager, fsrmscreen/IFsrmFileScreenManager
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
 - IFsrmFileScreenManager
 - fsrmscreen/IFsrmFileScreenManager
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
 - IFsrmFileScreenManager
---

# IFsrmFileScreenManager interface


## -description

Used to manage file screen objects.

To get this interface, call the 
    <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex">CoCreateInstanceEx</a> function. Use 
    <b>CLSID_FsrmFileScreenManager</b> as the class identifier and 
    <code>__uuidof(IFsrmFileScreenManager)</code> as the interface identifier. 
    For an example, see <a href="/previous-versions/windows/desktop/fsrm/defining-a-file-screen">Defining a File Screen</a>.

## -inheritance

The <b>IFsrmFileScreenManager</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFsrmFileScreenManager</b> also has these types of members:

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

<a href="/previous-versions/windows/desktop/fsrm/fsrm-interfaces">FSRM Interfaces</a>



<a href="/previous-versions/windows/desktop/fsrm/fsrmfilescreenmanager">FsrmFileScreenManager</a>
