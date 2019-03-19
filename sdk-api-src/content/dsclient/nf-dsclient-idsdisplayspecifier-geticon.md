---
UID: NF:dsclient.IDsDisplaySpecifier.GetIcon
title: IDsDisplaySpecifier::GetIcon (dsclient.h)
author: windows-sdk-content
description: The IDsDisplaySpecifier::GetIcon method obtains the icon for a given object class.
old-location: ad\idsdisplayspecifier_geticon.htm
tech.root: ad
ms.assetid: 7057779b-4176-41a3-bc7e-0d6958baf245
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DSGIF_DEFAULTISCONTAINER, DSGIF_GETDEFAULTICON, DSGIF_ISDISABLED, DSGIF_ISMASK, DSGIF_ISNORMAL, DSGIF_ISOPEN, GetIcon, GetIcon method [Active Directory], GetIcon method [Active Directory],IDsDisplaySpecifier interface, IDsDisplaySpecifier interface [Active Directory],GetIcon method, IDsDisplaySpecifier.GetIcon, IDsDisplaySpecifier::GetIcon, _glines_idsdisplayspecifier_geticon, ad.idsdisplayspecifier__geticon, ad.idsdisplayspecifier_geticon, dsclient/IDsDisplaySpecifier::GetIcon
ms.topic: method
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
req.lib: 
req.dll: Dsadmin.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dsadmin.dll
api_name:
 - IDsDisplaySpecifier.GetIcon
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDsDisplaySpecifier::GetIcon


## -description


The <b>IDsDisplaySpecifier::GetIcon</b> method obtains the icon for a given object class.


## -parameters




### -param pszObjectClass [in]

Pointer to a null-terminated Unicode string that contains the name of the object class to obtain the icon for. Examples of the object class name are "user" and "container".


### -param dwFlags [in]

Contains a set of flags that indicate the type of icon to retrieve. This can be a combination of one or more of the following values.



#### DSGIF_ISNORMAL

Obtains the normal  icon for the object class.



#### DSGIF_ISOPEN

Obtains the open  icon, such as an open folder, for the object class. If the object class does not have an open icon, this method attempts to obtain the normal icon for the object class.



#### DSGIF_ISDISABLED

Obtains the disabled icon, such as a disabled user, for the object class. If the object class does not have a disabled  icon, this method attempts to obtain the normal icon for the object class.



#### DSGIF_ISMASK

Used to mask off the <b>DSGIF_ISNORMAL</b>, <b>DSGIF_ISOPEN</b> and <b>DSGIF_ISDISABLED</b> flags.



#### DSGIF_GETDEFAULTICON

If no icon can be found for the object class, this method returns a default icon. If this flag is not specified and no icon can be found for the object class, this method returns <b>NULL</b>.



#### DSGIF_DEFAULTISCONTAINER

If no icon can be found for the object class, this method will return the container icon as the default icon. If this flag is not specified and no icon can be found for the object class, this method returns <b>NULL</b>.


### -param cxIcon [in]

Contains the desired width, in pixels, of the icon. This method obtains the icon that most closely matches this width.


### -param cyIcon [in]

Contains the desired height, in pixels, of the icon. This method obtains the icon that most closely matches this height.


## -returns



Returns a handle to the icon, if successful, or <b>NULL</b> otherwise. The caller must destroy this icon when it is no longer required by passing this handle to <a href="https://msdn.microsoft.com/en-us/library/ms648063(v=VS.85).aspx">DestroyIcon</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms648063(v=VS.85).aspx">DestroyIcon</a>



<a href="https://msdn.microsoft.com/f53d4425-5496-45f8-a09b-f163b63a29c8">Display Interfaces in Active Directory Domain Services</a>



<a href="https://msdn.microsoft.com/a6ac7006-73b8-4673-89d6-8285453481d3">IDsDisplaySpecifier</a>
 

 

