---
UID: NF:dsclient.IDsDisplaySpecifier.IsClassContainer
title: IDsDisplaySpecifier::IsClassContainer (dsclient.h)
description: Determines if a given object class is a container.
helpviewer_keywords: ["DSICCF_IGNORETREATASLEAF","IDsDisplaySpecifier interface [Active Directory]","IsClassContainer method","IDsDisplaySpecifier.IsClassContainer","IDsDisplaySpecifier::IsClassContainer","IsClassContainer","IsClassContainer method [Active Directory]","IsClassContainer method [Active Directory]","IDsDisplaySpecifier interface","_glines_idsdisplayspecifier_isclasscontainer","ad.idsdisplayspecifier__isclasscontainer","ad.idsdisplayspecifier_isclasscontainer","dsclient/IDsDisplaySpecifier::IsClassContainer"]
old-location: ad\idsdisplayspecifier_isclasscontainer.htm
tech.root: ad
ms.assetid: 1717200a-353b-413e-97a2-0742a95056d8
ms.date: 12/05/2018
ms.keywords: DSICCF_IGNORETREATASLEAF, IDsDisplaySpecifier interface [Active Directory],IsClassContainer method, IDsDisplaySpecifier.IsClassContainer, IDsDisplaySpecifier::IsClassContainer, IsClassContainer, IsClassContainer method [Active Directory], IsClassContainer method [Active Directory],IDsDisplaySpecifier interface, _glines_idsdisplayspecifier_isclasscontainer, ad.idsdisplayspecifier__isclasscontainer, ad.idsdisplayspecifier_isclasscontainer, dsclient/IDsDisplaySpecifier::IsClassContainer
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDsDisplaySpecifier::IsClassContainer
 - dsclient/IDsDisplaySpecifier::IsClassContainer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dsadmin.dll
api_name:
 - IDsDisplaySpecifier.IsClassContainer
---

# IDsDisplaySpecifier::IsClassContainer


## -description

The <b>IDsDisplaySpecifier::IsClassContainer</b> method determines if a given object class is a container.

## -parameters

### -param pszObjectClass [in]

Pointer to a null-terminated Unicode string that contains the name of the object class to determine if it is a container. Examples of the object class name are "user" and "container".

### -param pszADsPath [in]

Pointer to a null-terminated Unicode string that contains the <b>ADsPath</b> of a class object that can be bound to in the display specifier container and whose schema data can be obtained.

### -param dwFlags [in]

Contains flags that modify the behavior of this method. This can be zero or the following flag.



#### DSICCF_IGNORETREATASLEAF

The <b>treatAsLeaf</b> attribute in the display specifier is ignored and only the schema data is used to determine if the class is a container.

## -returns

Returns <b>TRUE</b> if the specified class is a container. Otherwise it returns <b>FALSE</b>.

## -remarks

The method uses the schema data and/or the <b>treatAsLeaf</b> attribute of the  display specifier to determine if an object class is a container. The object class is determined to be a container if the schema indicates that the class can contain other objects. The <b>treatAsLeaf</b> attribute of the display specifier can be used to override the schema indicator.

## -see-also

<a href="/windows/desktop/AD/display-interfaces-in-active-directory-domain-services">Display Interfaces in Active Directory Domain Services</a>



<a href="/windows/desktop/api/dsclient/nn-dsclient-idsdisplayspecifier">IDsDisplaySpecifier</a>