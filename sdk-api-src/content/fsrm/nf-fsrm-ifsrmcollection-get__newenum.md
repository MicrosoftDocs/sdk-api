---
UID: NF:fsrm.IFsrmCollection.get__NewEnum
title: IFsrmCollection::get__NewEnum (fsrm.h)
description: Retrieves the IUnknown pointer of a new IEnumVARIANT enumeration for the items in the collection.
helpviewer_keywords: ["IFsrmCollection interface [File Server Resource Manager]","_NewEnum property","IFsrmCollection._NewEnum","IFsrmCollection.get__NewEnum","IFsrmCollection::_NewEnum","IFsrmCollection::get__NewEnum","_NewEnum property [File Server Resource Manager]","_NewEnum property [File Server Resource Manager]","IFsrmCollection interface","fs.ifsrmcollection__newenum","fsrm.ifsrmcollection__newenum","fsrm/IFsrmCollection::_NewEnum","fsrm/IFsrmCollection::get__NewEnum","get__NewEnum"]
old-location: fsrm\ifsrmcollection__newenum.htm
tech.root: fsrm
ms.assetid: 0973b046-e350-44df-a02d-40b0ba272638
ms.date: 12/05/2018
ms.keywords: IFsrmCollection interface [File Server Resource Manager],_NewEnum property, IFsrmCollection._NewEnum, IFsrmCollection.get__NewEnum, IFsrmCollection::_NewEnum, IFsrmCollection::get__NewEnum, _NewEnum property [File Server Resource Manager], _NewEnum property [File Server Resource Manager],IFsrmCollection interface, fs.ifsrmcollection__newenum, fsrm.ifsrmcollection__newenum, fsrm/IFsrmCollection::_NewEnum, fsrm/IFsrmCollection::get__NewEnum, get__NewEnum
req.header: fsrm.h
req.include-header: FsrmQuota.h, FsrmReports.h, FsrmScreen.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.dll: SrmSvc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsrmCollection::get__NewEnum
 - fsrm/IFsrmCollection::get__NewEnum
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmCollection._NewEnum
 - IFsrmCollection.get__NewEnum
---

# IFsrmCollection::get__NewEnum


## -description

Retrieves the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointer of a new 
    <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a> enumeration for the items in 
    the collection.

This property is read-only.

## -parameters

## -remarks

C/C++ users use this method to enumerate items in the collection. Call the 
    <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> of the 
    <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface to get the 
    <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a> interface. Use the 
    <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-ienumvariant-next">IEnumVARIANT::Next</a> method to enumerate 
    the items of the collection. The items are returned as <b>VARIANT</b> values.

If the collection contains interfaces, the  variant type is <b>VT_DISPATCH</b>. Call the 
    <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method on the 
    <b>pdispVal</b> member of the variant to get an interface to the specific object. For example, 
    if the collection contains report objects, you would query the <b>pdispVal</b> member for the 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmreport">IFsrmReport</a> interface.

If the item is an <b>HRESULT</b> value, the variant type is 
    <b>VT_I4</b>. Use the <b>lVal</b> member of the variant to get the 
    <b>HRESULT</b> value.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmcollection">IFsrmCollection</a>