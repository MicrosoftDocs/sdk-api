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

# IShellView::CreateViewWindow


## -description


Creates a view window. This can be either the right pane of Windows Explorer or the client window of a folder window.


## -parameters




### -param psvPrevious [in]

Type: <b><a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a>*</b>

The address of the <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a> interface of the view window being exited. Views can use this parameter to communicate with a previous view of the same implementation. This interface can be used to optimize browsing between like views. This pointer may be <b>NULL</b>.


### -param pfs [in]

Type: <b>LPCFOLDERSETTINGS</b>

The address of a <a href="https://msdn.microsoft.com/be00fe39-1add-412e-b88b-4b0b1404b19d">FOLDERSETTINGS</a> structure. The view should use this when creating its view.


### -param psb [in]

Type: <b><a href="https://msdn.microsoft.com/138d90e3-a1f0-4faf-88ca-16c7a46df0ca">IShellBrowser</a>*</b>

The address of the current instance of the <a href="https://msdn.microsoft.com/138d90e3-a1f0-4faf-88ca-16c7a46df0ca">IShellBrowser</a> interface. The view should call this interface's <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> method and keep the interface pointer to allow communication with the Windows Explorer window.


### -param prcView [in]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>*</b>

The dimensions of the new view, in client coordinates.


### -param phWnd [out]

Type: <b>HWND*</b>

The address of the window handle being created.


## -returns



Type: <b>HRESULT</b>

Returns a success code if successful, or a COM error code otherwise. Use the <a href="com.succeeded">SUCCEEDED</a> and <a href="com.failed">FAILED</a> macros to determine whether the operation succeeded or failed.




## -remarks



<h3><a id="Notes_to_Calling_applications"></a><a id="notes_to_calling_applications"></a><a id="NOTES_TO_CALLING_APPLICATIONS"></a>Notes to Calling applications</h3>
Call this method when the view needs to be created.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Create your view window and restore any persistent state by calling the <a href="https://msdn.microsoft.com/887ebe9f-8bde-46dd-a7a2-7b2ca66bf905">GetViewStateStream</a> method. Store the <a href="https://msdn.microsoft.com/138d90e3-a1f0-4faf-88ca-16c7a46df0ca">IShellBrowser</a> pointer for further use.




## -see-also




<a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a>
 

 

