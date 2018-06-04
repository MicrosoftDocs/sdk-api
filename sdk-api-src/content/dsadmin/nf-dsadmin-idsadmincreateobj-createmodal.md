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

# IDsAdminCreateObj::CreateModal


## -description


The <b>IDsAdminCreateObj::CreateModal</b> method displays the object creation wizard and returns the newly created object. The <a href="https://msdn.microsoft.com/811863e7-25d2-48d0-bf97-61b49a224c98">IDsAdminCreateObj::Initialize</a> method must be called before <b>IDsAdminCreateObj::CreateModal</b> can be called.


## -parameters




### -param hwndParent [in]

Contains the window handle of the owner of the wizard. This value cannot be <b>NULL</b>. Use the result of the <a href="_win32_getdesktopwindow_cpp">GetDesktopWindow</a> function if no parent window is available.


### -param ppADsObj [out]

Pointer to an <a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a> interface pointer that receives the newly created object. This parameter receives <b>NULL</b> if the object creation wizard fails or is canceled. The caller must release this interface when it is no longer required. This parameter may be <b>NULL</b> if this object is not required.


## -returns



This method can return one of these values.


Returns an OLE-defined error code or one of the following values.






## -remarks



If the user cancels the object creation wizard, this method returns S_FALSE.  If <i>ppADsObj</i> is not <b>NULL</b>, <i>ppADsObj</i> receives a <b>NULL</b> value. Because of this, the use of the <a href="_com_succeeded">SUCCEEDED</a> macro to determine if <i>ppADsObj</i> is valid should be avoided. Always test the contents of <i>ppADsObj</i> for a non-<b>NULL</b> value before using the interface pointer.




## -see-also




<a href="_win32_getdesktopwindow_cpp">GetDesktopWindow</a>



<a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a>



<a href="https://msdn.microsoft.com/93673b29-744a-4100-86b7-8a2eec861c47">IDsAdminCreateObj</a>



<a href="https://msdn.microsoft.com/811863e7-25d2-48d0-bf97-61b49a224c98">IDsAdminCreateObj::Initialize</a>



<a href="_com_succeeded">SUCCEEDED</a>
 

 

