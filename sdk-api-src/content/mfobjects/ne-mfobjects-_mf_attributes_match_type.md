---
UID: NE:mfobjects._MF_ATTRIBUTES_MATCH_TYPE
title: "_MF_ATTRIBUTES_MATCH_TYPE"
author: windows-sdk-content
description: Specifies how to compare the attributes on two objects.
old-location: mf\mf_attributes_match_type.htm
old-project: medfound
ms.assetid: cfa534c4-88c3-4170-b977-c24ea5593f6c
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: MF_ATTRIBUTES_MATCH_ALL_ITEMS, MF_ATTRIBUTES_MATCH_INTERSECTION, MF_ATTRIBUTES_MATCH_OUR_ITEMS, MF_ATTRIBUTES_MATCH_SMALLER, MF_ATTRIBUTES_MATCH_THEIR_ITEMS, MF_ATTRIBUTES_MATCH_TYPE, MF_ATTRIBUTES_MATCH_TYPE enumeration [Media Foundation], _MF_ATTRIBUTES_MATCH_TYPE, cfa534c4-88c3-4170-b977-c24ea5593f6c, mf.mf_attributes_match_type, mfobjects/MF_ATTRIBUTES_MATCH_ALL_ITEMS, mfobjects/MF_ATTRIBUTES_MATCH_INTERSECTION, mfobjects/MF_ATTRIBUTES_MATCH_OUR_ITEMS, mfobjects/MF_ATTRIBUTES_MATCH_SMALLER, mfobjects/MF_ATTRIBUTES_MATCH_THEIR_ITEMS, mfobjects/MF_ATTRIBUTES_MATCH_TYPE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: mfobjects.h
req.include-header: Mfidl.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: MF_ATTRIBUTES_MATCH_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfobjects.h
api_name:
 - MF_ATTRIBUTES_MATCH_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MF_ATTRIBUTES_MATCH_TYPE enumeration


## -description



Specifies how to compare the attributes on two objects.




## -enum-fields




### -field MF_ATTRIBUTES_MATCH_OUR_ITEMS

Check whether all the attributes in <i>pThis</i> exist in <i>pTheirs</i> and have the same data, where <i>pThis</i> is the object whose <a href="https://msdn.microsoft.com/1d0c9d1c-448d-4851-b183-94b04acb2ab5">Compare</a> method is being called and <i>pTheirs</i> is the object given in the <i>pTheirs</i> parameter.


### -field MF_ATTRIBUTES_MATCH_THEIR_ITEMS

Check whether all the attributes in <i>pTheirs</i> exist in <i>pThis</i> and have the same data, where <i>pThis</i> is the object whose <a href="https://msdn.microsoft.com/1d0c9d1c-448d-4851-b183-94b04acb2ab5">Compare</a> method is being called and <i>pTheirs</i> is the object given in the <i>pTheirs</i> parameter.


### -field MF_ATTRIBUTES_MATCH_ALL_ITEMS

Check whether both objects have identical attributes with the same data.


### -field MF_ATTRIBUTES_MATCH_INTERSECTION

Check whether the attributes that exist in both objects have the same data.


### -field MF_ATTRIBUTES_MATCH_SMALLER

Find the object with the fewest number of attributes, and check if those attributes exist in the other object and have the same data.


## -see-also




<a href="https://msdn.microsoft.com/1d0c9d1c-448d-4851-b183-94b04acb2ab5">IMFAttributes::Compare</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

