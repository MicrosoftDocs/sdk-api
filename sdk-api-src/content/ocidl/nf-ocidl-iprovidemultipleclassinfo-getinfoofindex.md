---
UID: NF:ocidl.IProvideMultipleClassInfo.GetInfoOfIndex
title: IProvideMultipleClassInfo::GetInfoOfIndex (ocidl.h)
description: Retrieves the type information from the specified index.helpviewer_keywords: ["GetInfoOfIndex","GetInfoOfIndex method [COM]","GetInfoOfIndex method [COM]","IProvideMultipleClassInfo interface","IProvideMultipleClassInfo interface [COM]","GetInfoOfIndex method","IProvideMultipleClassInfo.GetInfoOfIndex","IProvideMultipleClassInfo::GetInfoOfIndex","MULTICLASSINFO_GETIIDPRIMARY","MULTICLASSINFO_GETIIDSOURCE","MULTICLASSINFO_GETNUMRESERVEDDISPIDS","MULTICLASSINFO_GETTYPEINFO","_com_iprovidemultipleclassinfo_getinfoofindex","com.iprovidemultipleclassinfo_getinfoofindex","ocidl/IProvideMultipleClassInfo::GetInfoOfIndex"]
old-location: com\iprovidemultipleclassinfo_getinfoofindex.htm
tech.root: com
ms.assetid: 084dfb9d-5545-4845-9959-1b054566adca
ms.date: 12/05/2018
ms.keywords: GetInfoOfIndex, GetInfoOfIndex method [COM], GetInfoOfIndex method [COM],IProvideMultipleClassInfo interface, IProvideMultipleClassInfo interface [COM],GetInfoOfIndex method, IProvideMultipleClassInfo.GetInfoOfIndex, IProvideMultipleClassInfo::GetInfoOfIndex, MULTICLASSINFO_GETIIDPRIMARY, MULTICLASSINFO_GETIIDSOURCE, MULTICLASSINFO_GETNUMRESERVEDDISPIDS, MULTICLASSINFO_GETTYPEINFO, _com_iprovidemultipleclassinfo_getinfoofindex, com.iprovidemultipleclassinfo_getinfoofindex, ocidl/IProvideMultipleClassInfo::GetInfoOfIndex
ms.topic: method
f1_keywords:
- ocidl/IProvideMultipleClassInfo.GetInfoOfIndex
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- OCIdl.h
api_name:
- IProvideMultipleClassInfo.GetInfoOfIndex
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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

The <a href="https://msdn.microsoft.com/">coclass</a> type information for the requested contributor. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypeinfo">ITypeInfo</a>.


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




<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-iprovidemultipleclassinfo">IProvideMultipleClassInfo</a>
 

 

