---
UID: NS:msctf.TF_PROPERTYVAL
title: TF_PROPERTYVAL (msctf.h)
description: The TF_PROPERTYVAL structure contains property value data. This structure is used with the IEnumTfPropertyValue::Next method.
helpviewer_keywords: ["TF_PROPERTYVAL","TF_PROPERTYVAL structure [Text Services Framework]","_tsf_tf_propertyval_ref","msctf/TF_PROPERTYVAL","tsf.tf_propertyval"]
old-location: tsf\tf_propertyval.htm
tech.root: TSF
ms.assetid: 50a5930c-ba17-4441-99a7-efc6c4bfc2ab
ms.date: 12/05/2018
ms.keywords: TF_PROPERTYVAL, TF_PROPERTYVAL structure [Text Services Framework], _tsf_tf_propertyval_ref, msctf/TF_PROPERTYVAL, tsf.tf_propertyval
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TF_PROPERTYVAL
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - TF_PROPERTYVAL
 - msctf/TF_PROPERTYVAL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Msctf.h
api_name:
 - TF_PROPERTYVAL
---

# TF_PROPERTYVAL structure


## -description

The <b>TF_PROPERTYVAL</b> structure contains property value data. This structure is used with the <a href="/windows/desktop/api/msctf/nf-msctf-ienumtfpropertyvalue-next">IEnumTfPropertyValue::Next</a> method.

## -struct-fields

### -field guidId

A <b>GUID</b> that identifies the property type. This can be a custom identifier or one of the <a href="/windows/desktop/TSF/predefined-properties">predefined property identifiers</a>.

### -field varValue

A <b>VARIANT</b> that contains the value of the property specified by <b>guidId</b>. The user must know the type and format of this data.

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-ienumtfpropertyvalue-next">IEnumTfPropertyValue::Next
      </a>



<a href="/windows/desktop/TSF/predefined-properties">Predefined Properties
      </a>