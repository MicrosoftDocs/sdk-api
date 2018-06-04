---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# TreeView_EndEditLabelNow macro


## -description


Ends the editing of a tree-view item's label. You can use this macro or send the <a href="https://msdn.microsoft.com/68de2020-9311-4958-859a-de55f5e41fcf">TVM_ENDEDITLABELNOW</a> message explicitly. 


## -parameters




### -param hwnd

TBD


### -param fCancel

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Variable that indicates whether the editing is canceled without being saved to the label. If this parameter is <b>TRUE</b>, the system cancels editing without saving the changes. Otherwise, the system saves the changes to the label. 


#### - hwndTV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 


## -remarks



This macro causes the <a href="https://msdn.microsoft.com/82eb9fcd-de10-4efb-8501-78c5af5e089e">TVN_ENDLABELEDIT</a> notification code to be sent to the parent window of the tree-view control. 



