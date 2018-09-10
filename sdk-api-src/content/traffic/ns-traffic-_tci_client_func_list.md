---
UID: NS:traffic._TCI_CLIENT_FUNC_LIST
title: "_TCI_CLIENT_FUNC_LIST"
author: windows-sdk-content
description: The TCI_CLIENT_FUNC_LIST structure is used by the traffic control interface to register and then access client-callback functions. Each member of TCI_CLIENT_FUNC_LIST is a pointer to the client provided&#8211;callback function.
old-location: qos\tci_client_func_list.htm
tech.root: QOS
ms.assetid: 45eccc44-d170-49cc-b51d-bb502c2fc1c7
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PTCI_CLIENT_FUNC_LIST, PTCI_CLIENT_FUNC_LIST, PTCI_CLIENT_FUNC_LIST structure pointer [QOS], TCI_CLIENT_FUNC_LIST, TCI_CLIENT_FUNC_LIST structure [QOS], _TCI_CLIENT_FUNC_LIST, _gqos_tci_client_func_list, qos.tci_client_func_list, traffic/PTCI_CLIENT_FUNC_LIST, traffic/TCI_CLIENT_FUNC_LIST"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: traffic.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Traffic.h
api_name:
 - TCI_CLIENT_FUNC_LIST
product: Windows
targetos: Windows
req.typenames: TCI_CLIENT_FUNC_LIST, *PTCI_CLIENT_FUNC_LIST
req.redist: 
---

# _TCI_CLIENT_FUNC_LIST structure


## -description


The 
<b>TCI_CLIENT_FUNC_LIST</b> structure is used by the traffic control interface to register and then access client-callback functions. Each member of 
<b>TCI_CLIENT_FUNC_LIST</b> is a pointer to the client provided–callback function.


## -struct-fields




### -field ClNotifyHandler

Pointer to the client-callback function 
<a href="https://msdn.microsoft.com/cacf4c21-d831-462c-b9e8-fd51fcf8e4e4">ClNotifyHandler</a>.


### -field ClAddFlowCompleteHandler

Pointer to the client-callback function <a href="https://msdn.microsoft.com/0aa6f590-f7b2-4312-87a7-3854f883fa22">ClAddFlowComplete</a>.


### -field ClModifyFlowCompleteHandler

Pointer to the client-callback function <a href="https://msdn.microsoft.com/61afc465-d942-4db7-96ee-56f3f1c3cafa">ClModifyFlowComplete</a>.


### -field ClDeleteFlowCompleteHandler

Pointer to the client-callback function <a href="https://msdn.microsoft.com/b31bd6e5-2b72-407d-a77e-ff9cee8de238">ClDeleteFlowComplete</a>.


## -remarks



Any member of the 
<b>TCI_CLIENT_FUNC_LIST</b> structure can be <b>NULL</b> except <b>ClNotifyHandler</b>.




## -see-also




<a href="https://msdn.microsoft.com/0aa6f590-f7b2-4312-87a7-3854f883fa22">ClAddFlowComplete</a>



<a href="https://msdn.microsoft.com/b31bd6e5-2b72-407d-a77e-ff9cee8de238">ClDeleteFlowComplete</a>



<a href="https://msdn.microsoft.com/61afc465-d942-4db7-96ee-56f3f1c3cafa">ClModifyFlowComplete</a>



<a href="https://msdn.microsoft.com/cacf4c21-d831-462c-b9e8-fd51fcf8e4e4">ClNotifyHandler</a>
 

 

