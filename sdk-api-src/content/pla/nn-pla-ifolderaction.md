---
UID: NN:pla.IFolderAction
title: IFolderAction (pla.h)
author: windows-sdk-content
description: Specifies the actions that the data manager is to take on each folder under the data collector set's root path if both conditions (age and size) are met. To get this interface, call the IFolderActionCollection::CreateFolderAction method.
old-location: pla\ifolderaction.htm
tech.root: PLA
ms.assetid: a3942d5f-9ec4-4461-84f9-f2fae3971e23
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFolderAction, IFolderAction interface [PLA], IFolderAction interface [PLA],described, base.ifolderaction, pla.ifolderaction, pla/IFolderAction
ms.topic: interface
req.header: pla.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Pla.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - IFolderAction
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFolderAction interface


## -description


Specifies the actions that the <a href="https://msdn.microsoft.com/a153d88f-4c7e-45fd-9cd8-497160711de4">data manager</a> is to take on each folder under the data collector set's <a href="https://msdn.microsoft.com/42940cec-c76a-433c-9308-f030dacb05a4">root path</a> if both conditions (age and size) are met. 

To get this interface, call the <a href="https://msdn.microsoft.com/caced576-cbe8-49d1-a372-70f035a6e3ed">IFolderActionCollection::CreateFolderAction</a> method.


## -remarks



To create the object from a script, use the Pla.FolderAction program identifier.

For an example that shows the XML that you can use to initialize this object if you call the <a href="https://msdn.microsoft.com/10bffd54-990f-412f-baae-b8ab621b02b8">IDataCollectorSet::SetXml</a> method, see the Remarks section of <a href="https://msdn.microsoft.com/a4ae0874-4ee6-46a1-9811-8cd4be26859c">IDataCollectorSet</a>.  When you specify the XML to create the object, you can specify only the elements for the properties that you want to set. If you do not specify a property, PLA provides a default value. When you retrieve the XML for the set, the XML includes all elements. 



