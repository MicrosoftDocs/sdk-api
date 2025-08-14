---
UID: NF:objbase.CoTreatAsClass
title: CoTreatAsClass function (objbase.h)
description: Establishes or removes an emulation, in which objects of one class are treated as objects of a different class.
helpviewer_keywords: ["CoTreatAsClass","CoTreatAsClass function [COM]","_com_CoTreatAsClass","com.cotreatasclass","objbase/CoTreatAsClass"]
old-location: com\cotreatasclass.htm
tech.root: com
ms.assetid: d871879f-ec68-48e1-8ef6-364cf1447d0f
ms.date: 12/05/2018
ms.keywords: CoTreatAsClass, CoTreatAsClass function [COM], _com_CoTreatAsClass, com.cotreatasclass, objbase/CoTreatAsClass
req.header: objbase.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CoTreatAsClass
 - objbase/CoTreatAsClass
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-com-ole32-l1-4-0.dll
 - ext-ms-win-com-ole32-l1-3-0.dll
 - ext-ms-win-com-ole32-l1-2-0.dll
 - ext-ms-win-com-ole32-l1-1-5.dll
 - ext-ms-win-com-ole32-l1-1-4.dll
 - ext-ms-win-com-ole32-l1-1-3.dll
 - ext-ms-win-com-ole32-l1-1-2.dll
 - ext-ms-win-com-ole32-l1-1-1.dll
 - ext-ms-win-com-ole32-l1-1-0.dll
 - api-ms-win-core-com-private-l1-3-1.dll
 - Ole32.dll
api_name:
 - CoTreatAsClass
---

# CoTreatAsClass function


## -description

Establishes or removes an emulation, in which objects of one class are treated as objects of a different class.

## -parameters

### -param clsidOld [in]

The CLSID of the object to be emulated.

### -param clsidNew [in]

The CLSID of the object that should emulate the original object. This replaces any existing emulation for <i>clsidOld</i>. This parameter can be CLSID_NULL, in which case any existing emulation for <i>clsidOld</i> is removed.

## -returns

This function can return the standard return values E_INVALIDARG, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The emulation was successfully established or removed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REGDB_E_CLASSNOTREG</b></dt>
</dl>
</td>
<td width="60%">
The <i>clsidOld</i> parameter is not properly registered in the registration database.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REGDB_E_READREGDB</b></dt>
</dl>
</td>
<td width="60%">
Error reading from registration database.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REGDB_E_WRITEREGDB</b></dt>
</dl>
</td>
<td width="60%">
Error writing to registration database.

</td>
</tr>
</table>

## -remarks

This function sets the <b>TreatAs</b> entry in the registry for the specified object, allowing the object to be emulated by another application. Emulation allows an application to open and edit an object of a different format, while retaining the original format of the object. After this entry is set, whenever any function such as <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject">CoGetClassObject</a> specifies the object's original CLSID (<i>clsidOld</i>), it is transparently forwarded to the new CLSID (<i>clsidNew</i>), thus launching the application associated with the <b>TreatAs</b> CLSID. When the object is saved, it can be saved in its native format, which may result in loss of edits not supported by the original format.

If your application supports emulation, call <b>CoTreatAsClass</b> in the following situations:

<ul>
<li>
In response to an end-user request (through a conversion dialog box) that a specified object be treated as an object of a different class (an object created under one application be run under another application, while retaining the original format information).

</li>
<li>
In a setup program, to register that one class of objects be treated as objects of a different class.

</li>
</ul>
An example of the first case is that an end user might wish to edit a spreadsheet created by one application using a different application that can read and write the spreadsheet format of the original application. For an application that supports emulation, <b>CoTreatAsClass</b> can be called to implement a <b>Treat As</b> option in a conversion dialog box.



An example of the use of <b>CoTreatAsClass</b> in a setup program would be in an updated version of an application. When the application is updated, the objects created with the earlier version can be activated and treated as objects of the new version, while retaining the previous format information. This would allow you to give the user the option to convert when they save, or to save it in the previous format, possibly losing format information not available in the older version.

One result of setting an emulation is that when you enumerate verbs, as in the <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-enumverbs">IOleObject::EnumVerbs</a> method implementation in the default handler, this would enumerate the verbs from <i>clsidNew</i> instead of <i>clsidOld</i>.



To ensure that existing emulation information is removed when you install an application, your setup programs should call <b>CoTreatAsClass</b>, setting the <i>clsidNew</i> parameter to CLSID_NULL to remove any existing emulation for the classes they install.

If there is no CLSID assigned to the <b>AutoTreatAs</b> key in the registry, setting <i>clsidNew</i> and <i>clsidOld</i> to the same value removes the <b>TreatAs</b> entry, so there is no emulation. If there is a CLSID assigned to the <b>AutoTreatAs</b> key, that CLSID is assigned to the <b>TreatAs</b> key.



<b>CoTreatAsClass</b> does not validate whether an appropriate registry entry for clsidNew currently exists.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogettreatasclass">CoGetTreatAsClass</a>