---
UID: NF:cmnquery.IQueryForm.Initialize
title: IQueryForm::Initialize (cmnquery.h)
description: Initializes the query form extension object.
helpviewer_keywords: ["IQueryForm interface [Active Directory]","Initialize method","IQueryForm.Initialize","IQueryForm::Initialize","Initialize","Initialize method [Active Directory]","Initialize method [Active Directory]","IQueryForm interface","_glines_iqueryform_initialize","ad.iqueryform__initialize","ad.iqueryform_initialize","cmnquery/IQueryForm::Initialize"]
old-location: ad\iqueryform_initialize.htm
tech.root: ad
ms.assetid: d1250c69-f29b-44f1-b123-13818d26e322
ms.date: 12/05/2018
ms.keywords: IQueryForm interface [Active Directory],Initialize method, IQueryForm.Initialize, IQueryForm::Initialize, Initialize, Initialize method [Active Directory], Initialize method [Active Directory],IQueryForm interface, _glines_iqueryform_initialize, ad.iqueryform__initialize, ad.iqueryform_initialize, cmnquery/IQueryForm::Initialize
req.header: cmnquery.h
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
req.lib: Uuid.lib
req.dll: Dsquery.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IQueryForm::Initialize
 - cmnquery/IQueryForm::Initialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dsquery.dll
api_name:
 - IQueryForm.Initialize
---

# IQueryForm::Initialize


## -description

The <b>IQueryForm::Initialize</b> method initializes the query form extension object.

## -parameters

### -param hkForm [in]

Contains a registry key that identifies where the query form object was obtained. This parameter may be <b>NULL</b>.

## -returns

This method returns <b>S_OK</b> to enable the form object within the query dialog, or a failure code, such as <b>E_FAIL</b>, to prevent the form from being added to the query dialog.

## -see-also

<a href="/windows/desktop/api/cmnquery/nn-cmnquery-iqueryform">IQueryForm</a>