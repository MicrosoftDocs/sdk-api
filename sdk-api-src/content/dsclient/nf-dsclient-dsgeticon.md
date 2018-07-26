---
UID: NF:dsclient.DsGetIcon
title: DsGetIcon function
author: windows-sdk-content
description: Obtains the icon for a given object class.
old-location: ad\dsgeticon.htm
old-project: ad
ms.assetid: eee18c78-aefa-4f09-9361-91893502efec
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: DSGIF_DEFAULTISCONTAINER, DSGIF_GETDEFAULTICON, DSGIF_ISDISABLED, DSGIF_ISNORMAL, DSGIF_ISOPEN, DsGetIcon, DsGetIcon function [Active Directory], ad.dsgeticon, dsclient/DsGetIcon
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: dsclient.h
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
tech.root: 
req.typenames: DSA_NEWOBJ_DISPINFO, *LPDSA_NEWOBJ_DISPINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dsuiext.dll
api_name:
 - DsGetIcon
product: Windows
targetos: Windows
req.lib: Dsuiext.lib
req.dll: Dsuiext.dll
req.irql: 
---

# DsGetIcon function


## -description


The <b>DsGetIcon</b> function obtains the icon for a given object class. This function is obsolete. New applications should use the <a href="https://msdn.microsoft.com/7057779b-4176-41a3-bc7e-0d6958baf245">IDsDisplaySpecifier::GetIcon</a> method to perform this function.


## -parameters




### -param dwFlags [in]

Contains a set of flags that indicate the type of icon to retrieve. This can be a combination of one or more of the following values.



#### DSGIF_ISNORMAL

Obtains the normal  icon for the object class.



#### DSGIF_ISOPEN

Obtains the open  icon, such as an open folder, for the object class. If the object class does not have an open icon, this function attempts to obtain the normal icon for the object class.



#### DSGIF_ISDISABLED

Obtains the disabled icon, such as a disabled user, for the object class. If the object class does not have a disabled  icon, this function attempts to obtain the normal icon for the object class.



#### DSGIF_GETDEFAULTICON

If no icon can be found for the object class, this function will return a default icon. If this flag is not specified and no icon can be found for the object class, this function returns <b>NULL</b>.



#### DSGIF_DEFAULTISCONTAINER

If no icon can be found for the object class, this function returns the container icon as the default icon. If this flag is not specified and no icon can be found for the object class, this function returns <b>NULL</b>.


### -param pszObjectClass [in]

Pointer to a null-terminated Unicode string that contains the name of the object class to retrieve the icon for. Examples of the object class name are "user" and "container".


### -param cxImage [in]

Contains the desired width, in pixels, of the icon. This function retrieves the icon that most closely matches this width.


### -param cyImage [in]

Contains the desired height, in pixels, of the icon. This function retrieves the icon that most closely matches this height.


## -returns



Returns a handle to the icon if successful or <b>NULL</b> otherwise. The caller must destroy this icon when it is no longer required by passing this handle to <a href="_win32_destroyicon_cpp">DestroyIcon</a>.




## -see-also




<a href="_win32_destroyicon_cpp">DestroyIcon</a>



<a href="https://msdn.microsoft.com/7057779b-4176-41a3-bc7e-0d6958baf245">IDsDisplaySpecifier::GetIcon</a>
 

 

