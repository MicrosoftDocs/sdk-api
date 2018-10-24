---
UID: NF:objsel.IDsObjectPicker.InvokeDialog
title: IDsObjectPicker::InvokeDialog
author: windows-sdk-content
description: Displays a modal object picker dialog box and returns the user selections.
old-location: ad\idsobjectpicker_invokedialog.htm
tech.root: ad
ms.assetid: 76192a35-10e1-46e3-8724-7637d47d8eca
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IDsObjectPicker interface [Active Directory],InvokeDialog method, IDsObjectPicker.InvokeDialog, IDsObjectPicker::InvokeDialog, InvokeDialog, InvokeDialog method [Active Directory], InvokeDialog method [Active Directory],IDsObjectPicker interface, _glines_idsobjectpicker_invokedialog, ad.idsobjectpicker__invokedialog, ad.idsobjectpicker_invokedialog, objsel/IDsObjectPicker::InvokeDialog
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: objsel.h
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
req.lib: 
req.dll: Objsel.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Objsel.dll
api_name:
 - IDsObjectPicker.InvokeDialog
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDsObjectPicker::InvokeDialog


## -description


The <b>IDsObjectPicker::InvokeDialog</b> method displays a modal object picker dialog box and returns the user selections.


## -parameters




### -param hwndParent

Handle to the owner window of the dialog box. This parameter cannot be <b>NULL</b> or the result of the <a href="https://msdn.microsoft.com/en-us/library/ms633504(v=VS.85).aspx">GetDesktopWindow</a> function.


### -param ppdoSelections

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms688421(v=VS.85).aspx">IDataObject</a> interface pointer that receives a data object that contains data about the user selections. This data is supplied in the <a href="https://msdn.microsoft.com/cd634e3b-0eb7-4144-b9e1-1d27a322f72c">CFSTR_DSOP_DS_SELECTION_LIST</a> data format. This parameter receives <b>NULL</b> if the user cancels the dialog box.


## -returns



Returns a standard error code or one of the following values.




## -remarks



Before <b>IDsObjectPicker::InvokeDialog</b> is called, the <a href="https://msdn.microsoft.com/f2f9da7d-7a09-4b49-a750-078a4573e213">IDsObjectPicker</a> object must be initialized by calling <a href="https://msdn.microsoft.com/bcf4d283-6709-4425-a122-8f0808502b58">IDsObjectPicker::Initialize</a>. After the <b>IDsObjectPicker</b> object is initialized, <b>InvokeDialog</b> can be called multiple times without reinitializing the interface.




## -see-also




<a href="https://msdn.microsoft.com/cd634e3b-0eb7-4144-b9e1-1d27a322f72c">CFSTR_DSOP_DS_SELECTION_LIST</a>



<a href="https://msdn.microsoft.com/7a587997-0423-450f-a845-bddf12b69fae">DS_SELECTION</a>



<a href="https://msdn.microsoft.com/15493b8c-014e-4e69-9e67-40b24d44606d">DS_SELECTION_LIST</a>



<a href="https://msdn.microsoft.com/5b3e5d71-afd2-49db-b3a2-f9a49f0b2b3a">Directory Object Picker</a>



<a href="https://msdn.microsoft.com/en-us/library/ms688421(v=VS.85).aspx">IDataObject</a>



<a href="https://msdn.microsoft.com/f2f9da7d-7a09-4b49-a750-078a4573e213">IDsObjectPicker</a>
 

 

