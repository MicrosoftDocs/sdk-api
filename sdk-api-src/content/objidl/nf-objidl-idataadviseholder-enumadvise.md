---
UID: NF:objidl.IDataAdviseHolder.EnumAdvise
title: IDataAdviseHolder::EnumAdvise (objidl.h)
description: Returns an object that can be used to enumerate the current advisory connections.
helpviewer_keywords: ["EnumAdvise","EnumAdvise method [COM]","EnumAdvise method [COM]","IDataAdviseHolder interface","IDataAdviseHolder interface [COM]","EnumAdvise method","IDataAdviseHolder.EnumAdvise","IDataAdviseHolder::EnumAdvise","_ole_idataadviseholder_enumadvise","com.idataadviseholder_enumadvise","objidl/IDataAdviseHolder::EnumAdvise"]
old-location: com\idataadviseholder_enumadvise.htm
tech.root: com
ms.assetid: 0863d013-6f55-40ce-92d2-68bb0455a911
ms.date: 12/05/2018
ms.keywords: EnumAdvise, EnumAdvise method [COM], EnumAdvise method [COM],IDataAdviseHolder interface, IDataAdviseHolder interface [COM],EnumAdvise method, IDataAdviseHolder.EnumAdvise, IDataAdviseHolder::EnumAdvise, _ole_idataadviseholder_enumadvise, com.idataadviseholder_enumadvise, objidl/IDataAdviseHolder::EnumAdvise
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - IDataAdviseHolder::EnumAdvise
 - objidl/IDataAdviseHolder::EnumAdvise
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IDataAdviseHolder.EnumAdvise
---

# IDataAdviseHolder::EnumAdvise


## -description

Returns an object that can be used to enumerate the current advisory connections.

## -parameters

### -param ppenumAdvise [out]

A pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-ienumstatdata">IEnumSTATDATA</a> pointer variable that receives the interface pointer to the new enumerator object. If the implementation returns <b>NULL</b> in *<i>ppenumAdvise</i>, there are no connections to advise sinks at this time.

## -returns

This method returns S_OK if the enumerator object is successfully instantiated or there are no connections.

## -remarks

This method must supply a pointer to an implementation of the <a href="/windows/desktop/api/objidl/nn-objidl-ienumstatdata">IEnumSTATDATA</a> interface. Its methods allow you to enumerate the data stored in an array of <a href="/windows/desktop/api/objidl/ns-objidl-statdata">STATDATA</a> structures. You get a pointer to the OLE implementation of <a href="/windows/desktop/api/objidl/nn-objidl-idataadviseholder">IDataAdviseHolder</a> through a call to <a href="/windows/desktop/api/ole2/nf-ole2-createdataadviseholder">CreateDataAdviseHolder</a>, and then call <b>IDataAdviseHolder::EnumAdvise</b> to implement <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-enumdadvise">IDataObject::EnumDAdvise</a>.

Adding more advisory connections while the enumerator object is active has an undefined effect on the enumeration that results from this method.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-idataadviseholder">IDataAdviseHolder</a>



<a href="/windows/desktop/api/objidl/nf-objidl-idataobject-enumdadvise">IDataObject::EnumDAdvise</a>



<a href="/windows/desktop/api/objidl/nn-objidl-ienumstatdata">IEnumSTATDATA</a>