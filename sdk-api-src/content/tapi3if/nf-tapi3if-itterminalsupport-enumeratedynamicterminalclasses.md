---
UID: NF:tapi3if.ITTerminalSupport.EnumerateDynamicTerminalClasses
title: ITTerminalSupport::EnumerateDynamicTerminalClasses (tapi3if.h)
description: The EnumerateDynamicTerminalClasses method enumerates the currently available dynamic terminal classes that are supported.
helpviewer_keywords: ["EnumerateDynamicTerminalClasses","EnumerateDynamicTerminalClasses method [TAPI 2.2]","EnumerateDynamicTerminalClasses method [TAPI 2.2]","ITTerminalSupport interface","ITTerminalSupport interface [TAPI 2.2]","EnumerateDynamicTerminalClasses method","ITTerminalSupport.EnumerateDynamicTerminalClasses","ITTerminalSupport::EnumerateDynamicTerminalClasses","_tapi3_itterminalsupport_enumeratedynamicterminalclasses","tapi3.itterminalsupport_enumeratedynamicterminalclasses","tapi3if/ITTerminalSupport::EnumerateDynamicTerminalClasses"]
old-location: tapi3\itterminalsupport_enumeratedynamicterminalclasses.htm
tech.root: tapi3
ms.assetid: 1dcb9163-306b-42fc-afb4-41b33d7e2d40
ms.date: 12/05/2018
ms.keywords: EnumerateDynamicTerminalClasses, EnumerateDynamicTerminalClasses method [TAPI 2.2], EnumerateDynamicTerminalClasses method [TAPI 2.2],ITTerminalSupport interface, ITTerminalSupport interface [TAPI 2.2],EnumerateDynamicTerminalClasses method, ITTerminalSupport.EnumerateDynamicTerminalClasses, ITTerminalSupport::EnumerateDynamicTerminalClasses, _tapi3_itterminalsupport_enumeratedynamicterminalclasses, tapi3.itterminalsupport_enumeratedynamicterminalclasses, tapi3if/ITTerminalSupport::EnumerateDynamicTerminalClasses
req.header: tapi3if.h
req.include-header: Tapi3.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITTerminalSupport::EnumerateDynamicTerminalClasses
 - tapi3if/ITTerminalSupport::EnumerateDynamicTerminalClasses
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tapi3if.h
api_name:
 - ITTerminalSupport.EnumerateDynamicTerminalClasses
---

# ITTerminalSupport::EnumerateDynamicTerminalClasses


## -description

The 
<b>EnumerateDynamicTerminalClasses</b> method enumerates the currently available dynamic 
<a href="/windows/desktop/Tapi/terminal-class">terminal classes</a> that are supported. This method is provided for C and C++ applications. Automation client applications, such as those written in Visual Basic, must use the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itterminalsupport-get_dynamicterminalclasses">get_DynamicTerminalClasses</a> method.

## -parameters

### -param ppTerminalClassEnumerator [out]

Pointer to an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminalclass">IEnumTerminalClass</a> enumerator. TAPI returns these classes as GUIDs.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppTerminalClassEnumerator</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>

## -remarks

An application calls this method to find out which dynamic terminal classes are supported by this address in a call to 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal">ITTerminalSupport::CreateTerminal</a>.

TAPI calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminalclass">IEnumTerminalClass</a> interface returned by <b>ITTerminalSupport::EnumerateDynamicTerminalClasses</b>. The application must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on the 
<b>IEnumTerminalClass</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/Tapi/address-object">Address Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminalsupport">ITTerminalSupport</a>



<b>Terminal Classes</b>



<a href="/windows/desktop/Tapi/terminal-object">Terminal Object</a>



<a href="/windows/desktop/Tapi/terminal-object-interfaces">Terminal Object Interfaces</a>



<a href="/windows/desktop/Tapi/terminal-class">terminal classes</a>