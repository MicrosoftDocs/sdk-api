---
UID: NF:fsrmscreen.IFsrmFileScreenBase.EnumActions
title: IFsrmFileScreenBase::EnumActions
author: windows-sdk-content
description: Enumerates all the actions for the file screen object.
old-location: fsrm\ifsrmfilescreenbase_enumactions.htm
old-project: Fsrm
ms.assetid: fbc22338-8271-407a-97c6-4a2329445979
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: EnumActions, EnumActions method [File Server Resource Manager], EnumActions method [File Server Resource Manager],IFsrmFileScreenBase interface, IFsrmFileScreenBase interface [File Server Resource Manager],EnumActions method, IFsrmFileScreenBase.EnumActions, IFsrmFileScreenBase::EnumActions, fs.ifsrmfilescreenbase_enumactions, fsrm.ifsrmfilescreenbase_enumactions, fsrmscreen/IFsrmFileScreenBase::EnumActions
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: fsrmscreen.h
req.include-header: FsrmScreen.h, FsrmTlb.h
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
tech.root: 
req.typenames: FsrmTemplateApplyOptions
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmFileScreenBase.EnumActions
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmFileScreenBase::EnumActions


## -description


Enumerates all the actions for the file screen object.


## -parameters




### -param actions [out]

An <a href="https://msdn.microsoft.com/6a0c5d8b-5fed-4c55-971c-43430e3c6a8d">IFsrmCollection</a> interface that contains a collection of actions that are defined for the object.

Each item of the collection is a <b>VARIANT</b> of type <b>VT_DISPATCH</b>. Query the <b>pdispVal</b> member for the <a href="https://msdn.microsoft.com/81bfae1d-7d09-4ddc-9669-1da40dc72fd4">IFsrmAction</a> interface. You can then use the <a href="https://msdn.microsoft.com/7ce0bafb-8076-4a0d-bd59-9e2d436f74c1">IFsrmAction::ActionType</a> property to determine the type of action.


## -returns



The method returns the following return values.




## -see-also




<a href="https://msdn.microsoft.com/9e52af8c-e03b-4b44-83bd-541fe1419d6c">IFsrmFileScreenBase</a>
 

 

