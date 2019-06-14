---
UID: NS:dsquery.__unnamed_struct_3
title: DSQUERYCLASSLIST (dsquery.h)
author: windows-sdk-content
description: The DSQUERYCLASSLIST structure describes a list of classes against which a directory service query is made.
old-location: ad\dsqueryclasslist.htm
tech.root: ad
ms.assetid: 96cc527f-490f-4701-b000-6a42db8715fc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPDSQUERYCLASSLIST, DSQUERYCLASSLIST, DSQUERYCLASSLIST structure [Active Directory], LPDSQUERYCLASSLIST, LPDSQUERYCLASSLIST structure pointer [Active Directory], _glines_dsqueryclasslist, ad.dsqueryclasslist, dsquery/DSQUERYCLASSLIST, dsquery/LPDSQUERYCLASSLIST"
ms.topic: struct
req.header: dsquery.h
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dsquery.h
api_name:
 - DSQUERYCLASSLIST
product: Windows
targetos: Windows
req.typenames: DSQUERYCLASSLIST, *LPDSQUERYCLASSLIST
req.redist: 
ms.custom: 19H1
---

# DSQUERYCLASSLIST structure


## -description


The <b>DSQUERYCLASSLIST</b> structure describes a list of classes against which a directory service query is made.


## -struct-fields




### -field cbStruct

Size, in bytes, of this structure.


### -field cClasses

Number of the classes in the array.


### -field offsetClass

Offset to the class names of Unicode strings.


## -remarks



The class list is retrieved by the form pages upon receiving a DSQPM_GETCLASSLIST page message.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/AD/display-structures-in-active-directory-domain-services">Active
  Directory Display Structures</a>
 

 

