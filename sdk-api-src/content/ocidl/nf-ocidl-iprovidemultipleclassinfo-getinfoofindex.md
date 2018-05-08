---
UID: NF:ocidl.IProvideMultipleClassInfo.GetInfoOfIndex
title: IProvideMultipleClassInfo::GetInfoOfIndex
author: windows-driver-content
description: Retrieves the type information from the specified index.
old-location: com\iprovidemultipleclassinfo_getinfoofindex.htm
old-project: com
ms.assetid: 084dfb9d-5545-4845-9959-1b054566adca
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: GetInfoOfIndex, GetInfoOfIndex method [COM], GetInfoOfIndex method [COM],IProvideMultipleClassInfo interface, IProvideMultipleClassInfo interface [COM],GetInfoOfIndex method, IProvideMultipleClassInfo.GetInfoOfIndex, IProvideMultipleClassInfo::GetInfoOfIndex, MULTICLASSINFO_GETIIDPRIMARY, MULTICLASSINFO_GETIIDSOURCE, MULTICLASSINFO_GETNUMRESERVEDDISPIDS, MULTICLASSINFO_GETTYPEINFO, _com_iprovidemultipleclassinfo_getinfoofindex, com.iprovidemultipleclassinfo_getinfoofindex, ocidl/IProvideMultipleClassInfo::GetInfoOfIndex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VIEWSTATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	OCIdl.h
api_name:
-	IProvideMultipleClassInfo.GetInfoOfIndex
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IProvideMultipleClassInfo::GetInfoOfIndex


## -description


Retrieves the type information from the specified index.


## -parameters




### -param iti [in]

The index of the type information for which you want to obtain information. Index 0 is the default interface of the extender object; index *pcti-1 is the index of the base object.


### -param dwFlags [in]

A bitfield indicating which out parameters are being requested. Indicating a particular flag results in the appropriate information being assigned to the associated out parameter. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MULTICLASSINFO_GETTYPEINFO"></a><a id="multiclassinfo_gettypeinfo"></a><dl>
<dt><b>MULTICLASSINFO_GETTYPEINFO</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Indicates a request for <i>pptiCoClass</i> information.

</td>
</tr>
<tr>
<td width="40%"><a id="MULTICLASSINFO_GETNUMRESERVEDDISPIDS"></a><a id="multiclassinfo_getnumreserveddispids"></a><dl>
<dt><b>MULTICLASSINFO_GETNUMRESERVEDDISPIDS</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Indicates a request for <i>pcdispidReserved</i> and <i>pdwTIFlags</i> information.

</td>
</tr>
<tr>
<td width="40%"><a id="MULTICLASSINFO_GETIIDPRIMARY"></a><a id="multiclassinfo_getiidprimary"></a><dl>
<dt><b>MULTICLASSINFO_GETIIDPRIMARY</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Indicates a request for <i>piidPrimary</i> information.

</td>
</tr>
<tr>
<td width="40%"><a id="MULTICLASSINFO_GETIIDSOURCE"></a><a id="multiclassinfo_getiidsource"></a><dl>
<dt><b>MULTICLASSINFO_GETIIDSOURCE</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Indicates a request for <i>piidSource</i> information.

</td>
</tr>
</table>
 


### -param pptiCoClass [out]

The <a href="https://msdn.microsoft.com/333d0904-ffa2-4d25-878d-7422bcd40582">coclass</a> type information for the requested contributor. See <a href="f3356463-3373-4279-bae1-953378aa2680">ITypeInfo</a>.


### -param pdwTIFlags [out]

The bitfield flag.


### -param pcdispidReserved [out]

The mumber of DISPIDs the default interface of <i>pptiCoClass</i> reserves for its own use. This number can be used to calculate the amount to offset DISPIDs in the reserved range implemented by the object this class is extending.


### -param piidPrimary [out]

The IID of the primary interface for the requested contributor.


### -param piidSource [out]

The IID of the default source interface for the requested contributor. 


## -returns



This method can return the standard return values E_INVALIDARG, E_POINTER, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/87407830-b34b-4d4e-a5cc-551f47cffb75">IProvideMultipleClassInfo</a>
 

 

