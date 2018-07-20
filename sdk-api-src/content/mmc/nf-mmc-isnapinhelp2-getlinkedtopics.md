---
UID: NF:mmc.ISnapinHelp2.GetLinkedTopics
title: ISnapinHelp2::GetLinkedTopics
author: windows-sdk-content
description: Enables a snap-in to specify the names and locations of any HTML Help files that are linked to the snap-in's Help file (specified in the GetHelpTopic method).
old-location: mmc\isnapinhelp2_getlinkedtopics.htm
old-project: mmc
ms.assetid: ceed0d9f-e1bf-4692-aadf-e924095cdfc8
ms.author: windowssdkdev
ms.date: 07/17/2018
ms.keywords: GetLinkedTopics, GetLinkedTopics method [MMC], GetLinkedTopics method [MMC],ISnapinHelp2 interface, ISnapinHelp2 interface [MMC],GetLinkedTopics method, ISnapinHelp2.GetLinkedTopics, ISnapinHelp2::GetLinkedTopics, _slate_isnapinhelp2_getlinkedtopics, mmc.isnapinhelp2_getlinkedtopics, mmc/ISnapinHelp2::GetLinkedTopics
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
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
req.typenames: MMC_VIEW_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - ISnapinHelp2.GetLinkedTopics
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ISnapinHelp2::GetLinkedTopics


## -description


The <b>ISnapinHelp2::GetLinkedTopics</b> method enables a snap-in to specify the names and locations of any HTML Help files that are linked to the snap-in's Help file (specified in the 
<a href="https://msdn.microsoft.com/252403ef-6814-4ec0-bfef-ce5ca088bf41">GetHelpTopic</a> method).


## -parameters




### -param lpCompiledHelpFiles [out]

A pointer to the address of the null-terminated Unicode string that contains the path of one or more compiled Help files (.chm) that are linked to the snap-in's Help file. A semicolon is used to separate multiple file paths from each other.

When specifying the path, place the file anywhere and specify the full path name.


## -returns



This method can return one of these values.




## -remarks



MMC calls the snap-in's <b>ISnapinHelp2::GetLinkedTopics</b> method only if the snap-in returned <b>S_OK</b> from the 
<a href="https://msdn.microsoft.com/a7157e34-6f38-4589-b85e-8aca2bcd6ee1">ISnapinHelp2::GetHelpTopic</a> method call.

Allocate the <i>lpCompiledHelpFiles</i> string with the COM API function <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a> (or the equivalent) and MMC will release it




## -see-also




<a href="https://msdn.microsoft.com/87387cf5-ff5f-4816-8c96-97a7ae25df94">Adding HTML Help Support</a>



<a href="https://msdn.microsoft.com/6e86a22b-03b0-4ca6-a4e2-96ea365dabdf">ISnapinHelp2</a>



<a href="https://msdn.microsoft.com/a7157e34-6f38-4589-b85e-8aca2bcd6ee1">ISnapinHelp2::GetHelpTopic</a>
 

 

