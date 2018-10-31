---
UID: NF:shobjidl_core.IFolderView2.SetExtendedTileViewProperties
title: IFolderView2::SetExtendedTileViewProperties
author: windows-sdk-content
description: Sets the list of extended tile properties for an item.
old-location: shell\IFolderView2_SetExtendedTileViewProperties.htm
tech.root: shell
ms.assetid: efb2eb1a-47fa-45b2-8d8d-fc75bbe46c80
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IFolderView2 interface [Windows Shell],SetExtendedTileViewProperties method, IFolderView2.SetExtendedTileViewProperties, IFolderView2::SetExtendedTileViewProperties, SetExtendedTileViewProperties, SetExtendedTileViewProperties method [Windows Shell], SetExtendedTileViewProperties method [Windows Shell],IFolderView2 interface, _shell_IFolderView2_SetExtendedTileViewProperties, shell.IFolderView2_SetExtendedTileViewProperties, shobjidl_core/IFolderView2::SetExtendedTileViewProperties
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
 - IFolderView2.SetExtendedTileViewProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFolderView2::SetExtendedTileViewProperties


## -description


<p class="CCE_Message">[This method is still implemented, but should be considered deprecated as of Windows 7. It might not be implemented in future versions of Windows. It cannot be used with items in search results or library views, so consider using the item's existing properties or, if applicable, emitting properties from your namespace or property handler. See <a href="_search_3x_WDS_ExtIdx_PropertyHandlers">Developing Property Handlers for Windows Search</a> for more information.]

Sets the list of extended tile properties for an item.
        
            


## -parameters




### -param pidl [in]

Type: <b>PCUITEMID_CHILD</b>

A pointer to an item identifier list (PIDL).


### -param pszPropList [in]

Type: <b>LPCWSTR</b>

A pointer to a Unicode string containing a list of properties.


## -returns



Type: <b>DEPRECATED_HRESULT</b>

Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



The <i>pszPropList</i> parameter must be of the form "prop:&lt;canonical-property-name&gt;;&lt;canonical-property-name&gt;" where "&lt;canonical-property-name&gt;" is an actual canonical property name.  It can contain one or more properties delimited by semicolons.




## -see-also




<a href="https://msdn.microsoft.com/52fcf0df-f532-4114-b1c9-96838f1a5e77">IFolderView2</a>



<a href="https://msdn.microsoft.com/cac93c31-d90d-4116-b846-0cf593d1d56e">Property Description Schema</a>



<a href="https://msdn.microsoft.com/b7af0491-2ece-42b5-8eea-32643854632f">Property Lists</a>
 

 

