---
UID: NS:imepad.tagAPPLETIDLIST
title: APPLETIDLIST
author: windows-sdk-content
description: Specifies an IImePadApplet IID list.
old-location: intl\appletidlist.htm
tech.root: Intl
ms.assetid: 6A93B726-1C35-4779-AF60-859DF3B18462
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPAPPLETIDLIST, APPLETIDLIST, APPLETIDLIST structure [Internationalization for Windows Applications], PAPPLETIDLIST, PAPPLETIDLIST structure pointer [Internationalization for Windows Applications], imepad/APPLETIDLIST, imepad/PAPPLETIDLIST, intl.appletidlist"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: imepad.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Imepad.h
api_name:
 - APPLETIDLIST
product: Windows
targetos: Windows
req.typenames: APPLETIDLIST, *LPAPPLETIDLIST
req.redist: 
---

# APPLETIDLIST structure


## -description


Specifies an <a href="https://msdn.microsoft.com/F3BC7176-9659-47B6-AFCA-049807394961">IImePadApplet</a> IID list.


## -struct-fields




### -field count

The number of the IID's implemented in this applet.


### -field pIIDList

The IID list. This must be allocated with <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a>.

