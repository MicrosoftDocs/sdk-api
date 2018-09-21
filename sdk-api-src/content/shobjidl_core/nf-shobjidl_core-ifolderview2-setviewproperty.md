---
UID: NF:shobjidl_core.IFolderView2.SetViewProperty
title: IFolderView2::SetViewProperty
author: windows-sdk-content
description: Caches a property for an item in the view's property cache.
old-location: shell\IFolderView2_SetViewProperty.htm
tech.root: shell
ms.assetid: 76d91df0-8c90-45dc-9637-910b0874e9fa
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: IFolderView2 interface [Windows Shell],SetViewProperty method, IFolderView2.SetViewProperty, IFolderView2::SetViewProperty, SetViewProperty, SetViewProperty method [Windows Shell], SetViewProperty method [Windows Shell],IFolderView2 interface, _shell_IFolderView2_SetViewProperty, shell.IFolderView2_SetViewProperty, shobjidl_core/IFolderView2::SetViewProperty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - shobjidl_core.h
api_name:
 - IFolderView2.SetViewProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFolderView2::SetViewProperty


## -description


<p class="CCE_Message">[This method is still implemented, but should be considered deprecated as of Windows 7. It might not be implemented in future versions of Windows. It cannot be used with items in search results or library views, so consider using the item's existing properties or, if applicable, emitting properties from your namespace or property handler. See <a href="https://msdn.microsoft.com/en-us/library/Bb266532(v=VS.85).aspx">Developing Property Handlers for Windows Search</a> for more information.]

Caches a property for an item in the view's property cache.
        
            


## -parameters




### -param pidl [in]

Type: <b>PCUITEMID_CHILD</b>

A PIDL that identifies the item.


### -param propkey [in]

Type: <b>REFPROPERTYKEY</b>

The <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a> which is to be stored.


### -param propvar

TBD




#### - ppropvar [in]

Type: <b>const <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure in which the <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a> is stored.


## -returns



Type: <b>DEPRECATED_HRESULT</b>

Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



The property is displayed in the view, but not written to the underlying item.




## -see-also




<a href="https://msdn.microsoft.com/52fcf0df-f532-4114-b1c9-96838f1a5e77">IFolderView2</a>



<a href="https://msdn.microsoft.com/cac93c31-d90d-4116-b846-0cf593d1d56e">Property Description Schema</a>



<a href="https://msdn.microsoft.com/b7af0491-2ece-42b5-8eea-32643854632f">Property Lists</a>
 

 

