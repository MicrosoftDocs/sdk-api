---
UID: NS:commctrl.tagNMOBJECTNOTIFY
title: tagNMOBJECTNOTIFY
author: windows-sdk-content
description: Contains information used with the TBN_GETOBJECT, TCN_GETOBJECT, and PSN_GETOBJECT notification codes.
old-location: controls\NMOBJECTNOTIFY.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\common\structures\nmobjectnotify.htm
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: "*LPNMOBJECTNOTIFY, LPNMOBJECTNOTIFY, LPNMOBJECTNOTIFY structure pointer [Windows Controls], NMOBJECTNOTIFY, NMOBJECTNOTIFY structure [Windows Controls], _win32_NMOBJECTNOTIFY, _win32_NMOBJECTNOTIFY_cpp, commctrl/LPNMOBJECTNOTIFY, commctrl/NMOBJECTNOTIFY, controls.NMOBJECTNOTIFY, controls._win32_NMOBJECTNOTIFY, tagNMOBJECTNOTIFY"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: NMOBJECTNOTIFY, *LPNMOBJECTNOTIFY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	NMOBJECTNOTIFY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# tagNMOBJECTNOTIFY structure


## -description


Contains information used with the <a href="https://msdn.microsoft.com/9fd8516d-fe2e-4f84-9035-e2246aba369a">TBN_GETOBJECT</a>, <a href="https://msdn.microsoft.com/0beddabe-0e97-4fe7-bcf7-adaba0d72dfe">TCN_GETOBJECT</a>, and <a href="https://msdn.microsoft.com/179ac47c-9b32-4682-866d-1a1fad85080c">PSN_GETOBJECT</a> notification codes. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>

An <a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure that contains additional information about this notification. 


### -field iItem

Type: <b>int</b>

A control-specific item identifier. This value will comply to item identification standards for the control sending the notification. However, this member is not used with the <a href="https://msdn.microsoft.com/179ac47c-9b32-4682-866d-1a1fad85080c">PSN_GETOBJECT</a> notification code. 


### -field piid

Type: <b>IID*</b>

A pointer to an interface identifier of the requested object. 


### -field pObject

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to an object provided by the window processing the notification code. The application processing the notification code sets this member. 


### -field hResult

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

COM success or failure flags. The application processing the notification code sets this member. 


### -field dwFlags

 



