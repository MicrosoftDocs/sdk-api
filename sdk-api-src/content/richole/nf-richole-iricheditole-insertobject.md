---
UID: NF:richole.IRichEditOle.InsertObject
title: IRichEditOle::InsertObject
author: windows-sdk-content
description: Inserts an object into a rich edit control.
old-location: controls\IRichEditOle_InsertObject.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditinterfaces\iricheditole\iricheditoleinsertobject.htm
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IRichEditOle interface [Windows Controls],InsertObject method, IRichEditOle.InsertObject, IRichEditOle::InsertObject, InsertObject, InsertObject method [Windows Controls], InsertObject method [Windows Controls],IRichEditOle interface, _win32_IRichEditOle_InsertObject, _win32_IRichEditOle_InsertObject_cpp, controls.IRichEditOle_InsertObject, controls._win32_IRichEditOle_InsertObject, richole/IRichEditOle::InsertObject
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: richole.h
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
req.lib: 
req.dll: Msftedit.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - IRichEditOle.InsertObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRichEditOle::InsertObject


## -description


Inserts an object into a rich edit control.


## -parameters




### -param lpreobject

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb787946(v=VS.85).aspx">REOBJECT</a>*</b>

The object information and interfaces. The rich edit control automatically increments the reference count for the interfaces if it holds onto them, so the caller can safely release the interfaces if they are not needed. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK on success, or a failure code otherwise. E_OUTOFMEMORY is returned if memory could not be allocated to insert the object.




## -remarks



If the <b>cp</b> member of the <a href="https://msdn.microsoft.com/en-us/library/Bb787946(v=VS.85).aspx">REOBJECT</a> structure is REO_CP_SELECTION, the selection is replaced with the specified object.
	




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb774306(v=VS.85).aspx">IRichEditOle</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787946(v=VS.85).aspx">REOBJECT</a>



<b>Reference</b>
 

 

