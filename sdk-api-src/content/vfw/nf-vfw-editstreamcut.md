---
UID: NF:vfw.EditStreamCut
title: EditStreamCut function (vfw.h)
author: windows-sdk-content
description: The EditStreamCut function deletes all or part of an editable stream and creates a temporary editable stream from the deleted portion of the stream.
old-location: multimedia\editstreamcut.htm
tech.root: Multimedia
ms.assetid: 201f977c-926b-470c-b1ae-62946e6f691e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EditStreamCut, EditStreamCut function [Windows Multimedia], _win32_EditStreamCut, multimedia.editstreamcut, vfw/EditStreamCut
ms.topic: function
req.header: vfw.h
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
req.lib: Vfw32.lib
req.dll: Avifil32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Avifil32.dll
api_name:
 - EditStreamCut
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EditStreamCut function


## -description



The <b>EditStreamCut</b> function deletes all or part of an editable stream and creates a temporary editable stream from the deleted portion of the stream.




## -parameters




### -param pavi

Handle to the stream being edited.


### -param plStart

Starting position of the data to cut from the stream referenced by <i>pavi</i>.


### -param plLength

Amount of data to cut from the stream referenced by <i>pavi</i>.


### -param ppResult

Pointer to the handle created for the new stream.


## -returns



Returns zero if successful or an error otherwise.




## -remarks



The stream being edited must have been created by the <b>CreateEditableStream</b> function or one of the stream editing functions.

The temporary stream is an editable stream and can be treated as any other AVI stream. An application must release the temporary stream to free the resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>
 

 

