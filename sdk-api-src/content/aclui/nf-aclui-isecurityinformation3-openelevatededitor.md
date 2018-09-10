---
UID: NF:aclui.ISecurityInformation3.OpenElevatedEditor
title: ISecurityInformation3::OpenElevatedEditor
author: windows-sdk-content
description: Opens an access control editor when a user clicks the Edit button on an access control editor page that displays an image of a shield on that Edit button.
old-location: security\isecurityinformation3_openelevatededitor.htm
tech.root: SecAuthZ
ms.assetid: 4ed50e6b-4c4a-48bf-ad7c-133064a4be47
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ISecurityInformation3 interface [Security],OpenElevatedEditor method, ISecurityInformation3.OpenElevatedEditor, ISecurityInformation3::OpenElevatedEditor, OpenElevatedEditor, OpenElevatedEditor method [Security], OpenElevatedEditor method [Security],ISecurityInformation3 interface, aclui/ISecurityInformation3::OpenElevatedEditor, security.isecurityinformation3_openelevatededitor
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: aclui.h
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Aclui.h
api_name:
 - ISecurityInformation3.OpenElevatedEditor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISecurityInformation3::OpenElevatedEditor


## -description


The <b>OpenElevatedEditor</b> method opens an access control editor when a user clicks the <b>Edit</b> button on an access control editor page that displays an image of a shield on that <b>Edit</b> button. The image of a shield is displayed when the access control editor is launched by a process with a token that lacks permission to save changes to the object being edited.


## -parameters




### -param hWnd [in]

The parent window of the access control editor.


### -param uPage [in]

A value of the <a href="https://msdn.microsoft.com/122b2dcb-5557-4692-a0d6-4a0accf71740">SI_PAGE_TYPE</a> enumeration that indicates the page type on which to display the elevated access control editor.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/a22b9a75-6aa8-4b32-8d86-7fb21afd248f">GetFullResourceName</a>



<a href="https://msdn.microsoft.com/e6cf92da-ebd2-4960-9df1-7124745df616">ISecurityInformation3</a>
 

 

