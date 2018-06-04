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

# _tagIE4COMPONENT structure


## -description


Used by Microsoft Internet Explorer 4.0 and Microsoft Internet Explorer 4.01 to hold information about a component. With Windows 2000, it is replaced by the <a href="https://msdn.microsoft.com/library/windows/hardware/ff546180">COMPONENT</a> structure.


## -struct-fields




### -field dwSize

Type: <b>DWORD</b>

The size of the structure.


### -field dwID

Type: <b>DWORD</b>

Reserved. Set to zero.


### -field iComponentType

Type: <b>int</b>

The component type. It can be set to one of these values: 



#### COMP_TYPE_HTMLDOC



#### COMP_TYPE_PICTURE



#### COMP_TYPE_WEBSITE



#### COMP_TYPE_CONTROL


### -field fChecked

Type: <b>BOOL</b>

A value that is set to <b>TRUE</b> if the component is enabled, or <b>FALSE</b> if not.


### -field fDirty

Type: <b>BOOL</b>

A value that is set to <b>TRUE</b> if the component has been modified and not yet saved to disk. It will be set to <b>FALSE</b> if the component has not been modified, or if it has been modified and saved to disk.


### -field fNoScroll

Type: <b>BOOL</b>

A value that is set to <b>TRUE</b> if the component is scrollable, or <b>FALSE</b> if it's not.


### -field cpPos

Type: <b><a href="https://msdn.microsoft.com/622bdf51-d605-4eb9-a692-09be028bbff8">COMPPOS</a></b>

A <a href="https://msdn.microsoft.com/622bdf51-d605-4eb9-a692-09be028bbff8">COMPPOS</a> structure containing position and size information.


### -field wszFriendlyName

Type: <b>WCHAR[MAX_PATH]</b>

The component's friendly name.


### -field wszSource

Type: <b>WCHAR[INTERNET_MAX_URL_LENGTH]</b>

The component's URL.


### -field wszSubscribedURL

Type: <b>WCHAR[INTERNET_MAX_URL_LENGTH]</b>

The URL that a user has been subscribed to.

