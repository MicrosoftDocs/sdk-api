---
UID: NF:wbemcli.IWbemObjectTextSrc.GetText
title: IWbemObjectTextSrc::GetText (wbemcli.h)
description: The IWbemObjectTextSrc::GetText method creates a textual representation of an IWbemClassObject object; for example, an XML representation.
helpviewer_keywords: ["ExcludeSystemProperties","GetText","GetText method [Windows Management Instrumentation]","GetText method [Windows Management Instrumentation]","IWbemObjectTextSrc interface","IWbemObjectTextSrc interface [Windows Management Instrumentation]","GetText method","IWbemObjectTextSrc.GetText","IWbemObjectTextSrc::GetText","IncludeClassOrigin","IncludeQualifiers","LocalOnly","PathLevel","WMI_OBJ_TEXT_CIM_DTD_2_0","WMI_OBJ_TEXT_LAST","WMI_OBJ_TEXT_WMI_DTD_2_0","WMI_OBJ_TEXT_WMI_EXT1","WMI_OBJ_TEXT_WMI_EXT10","WMI_OBJ_TEXT_WMI_EXT2","WMI_OBJ_TEXT_WMI_EXT3","WMI_OBJ_TEXT_WMI_EXT4","WMI_OBJ_TEXT_WMI_EXT5","WMI_OBJ_TEXT_WMI_EXT6","WMI_OBJ_TEXT_WMI_EXT7","WMI_OBJ_TEXT_WMI_EXT8","WMI_OBJ_TEXT_WMI_EXT9","_hmm_iwbemobjecttextsrc_gettext","wbemcli/IWbemObjectTextSrc::GetText","wmi.iwbemobjecttextsrc_gettext"]
old-location: wmi\iwbemobjecttextsrc_gettext.htm
tech.root: wmi
ms.assetid: d4c36d19-cf28-43d3-a60a-50970d66bc17
ms.date: 12/05/2018
ms.keywords: ExcludeSystemProperties, GetText, GetText method [Windows Management Instrumentation], GetText method [Windows Management Instrumentation],IWbemObjectTextSrc interface, IWbemObjectTextSrc interface [Windows Management Instrumentation],GetText method, IWbemObjectTextSrc.GetText, IWbemObjectTextSrc::GetText, IncludeClassOrigin, IncludeQualifiers, LocalOnly, PathLevel, WMI_OBJ_TEXT_CIM_DTD_2_0, WMI_OBJ_TEXT_LAST, WMI_OBJ_TEXT_WMI_DTD_2_0, WMI_OBJ_TEXT_WMI_EXT1, WMI_OBJ_TEXT_WMI_EXT10, WMI_OBJ_TEXT_WMI_EXT2, WMI_OBJ_TEXT_WMI_EXT3, WMI_OBJ_TEXT_WMI_EXT4, WMI_OBJ_TEXT_WMI_EXT5, WMI_OBJ_TEXT_WMI_EXT6, WMI_OBJ_TEXT_WMI_EXT7, WMI_OBJ_TEXT_WMI_EXT8, WMI_OBJ_TEXT_WMI_EXT9, _hmm_iwbemobjecttextsrc_gettext, wbemcli/IWbemObjectTextSrc::GetText, wmi.iwbemobjecttextsrc_gettext
req.header: wbemcli.h
req.include-header: Wbemidl.h
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
req.lib: Wbemuuid.lib
req.dll: Fastprox.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemObjectTextSrc::GetText
 - wbemcli/IWbemObjectTextSrc::GetText
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fastprox.dll
api_name:
 - IWbemObjectTextSrc.GetText
---

# IWbemObjectTextSrc::GetText


## -description

The <b>IWbemObjectTextSrc::GetText</b> method creates a textual representation of an 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a> object; for example, an XML representation.

## -parameters

### -param lFlags

Reserved. Must be 0L.

### -param pObj

Reference to the object to be represented in text format. This parameter cannot be <b>NULL</b>.

### -param uObjTextFormat

Definition of the text format used to represent the object. For more information about valid values for this parameter, see Remarks.



#### WMI_OBJ_TEXT_CIM_DTD_2_0 (1 (0x1))

Use the DTD that corresponds to CIM DTD version 2.0.



#### WMI_OBJ_TEXT_WMI_DTD_2_0 (2 (0x2))

Use the WMI DTD that corresponds to CIM DTD version 2.0. Using this value enables WMI-specific extensions, such as embedded objects or scope.



#### WMI_OBJ_TEXT_WMI_EXT1 (3 (0x3))

Reserved for future use.



#### WMI_OBJ_TEXT_WMI_EXT2 (4 (0x4))

Reserved for future use.



#### WMI_OBJ_TEXT_WMI_EXT3 (5 (0x5))

Reserved for future use.



#### WMI_OBJ_TEXT_WMI_EXT4 (6 (0x6))

Reserved for future use.



#### WMI_OBJ_TEXT_WMI_EXT5 (7 (0x7))

Reserved for future use.



#### WMI_OBJ_TEXT_WMI_EXT6 (8 (0x8))

Reserved for future use.



#### WMI_OBJ_TEXT_WMI_EXT7 (9 (0x9))

Reserved for future use.



#### WMI_OBJ_TEXT_WMI_EXT8 (10 (0xA))

Reserved for future use.



#### WMI_OBJ_TEXT_WMI_EXT9 (11 (0xB))

Reserved for future use.



#### WMI_OBJ_TEXT_WMI_EXT10 (12 (0xC))

Reserved for future use.



#### WMI_OBJ_TEXT_LAST (13 (0xD))

Reserved for future use.

### -param pCtx

Optional. Context object for the operation. The context object can be used to specify whether  certain parts of the object are represented in text; for example, whether to include qualifiers in the textual representation. The context object takes the following optional values.



#### LocalOnly (VT_BOOL)

If <b>TRUE</b>, only locally defined properties and methods are present in the resulting XML. The default is <b>FALSE</b>.



#### IncludeQualifiers (VT_BOOL)

If <b>TRUE</b>, the qualifiers of classes, instances, properties, and methods are included in the output. The default is <b>FALSE</b>.



#### PathLevel (VT_I4)

The default is 0 (zero).

Possible values are:

<ul>
<li>
0

A <b>CLASS</b> or <b>INSTANCE</b> element is created depending on whether the object is a class or instance.

</li>
<li>
1

A <b>VALUE.NAMEDOBJECT</b> element is generated.

</li>
<li>
2

A VALUE.<b>OBJECTWITHLOCALPATH</b> element is generated.

</li>
<li>
3

A <b>VALUE.OBJECTWITHPATH</b> element is generated.

</li>
</ul>


#### ExcludeSystemProperties (VT_BOOL)

If <b>TRUE</b>, system properties, like <a href="/windows/desktop/WmiSdk/--namespace">__NAMESPACE</a>, are absent in the output. The default is <b>FALSE</b>.



#### IncludeClassOrigin (VT_BOOL)

If <b>TRUE</b>, the class origin attribute is set on <b>PROPERTY</b> and <b>METHOD</b> elements. The default is <b>FALSE</b>.

### -param strText

Textual representation of the object. User must free the string using <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> when finished with <i>strText</i>.

## -returns

This method returns an <b>HRESULT</b> that indicates the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

## -remarks

For more information, see 
<a href="/windows/desktop/WmiSdk/representing-objects-in-xml">Representing Objects in XML</a>.