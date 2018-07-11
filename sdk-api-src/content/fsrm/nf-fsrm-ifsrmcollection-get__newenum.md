---
UID: NF:fsrm.IFsrmCollection.get__NewEnum
title: IFsrmCollection::get__NewEnum
author: windows-sdk-content
description: Retrieves the IUnknown pointer of a new IEnumVARIANT enumeration for the items in the collection.
old-location: fsrm\ifsrmcollection__newenum.htm
old-project: fsrm
ms.assetid: 0973b046-e350-44df-a02d-40b0ba272638
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: IFsrmCollection interface [File Server Resource Manager],_NewEnum property, IFsrmCollection._NewEnum, IFsrmCollection.get__NewEnum, IFsrmCollection::_NewEnum, IFsrmCollection::get__NewEnum, _NewEnum property [File Server Resource Manager], _NewEnum property [File Server Resource Manager],IFsrmCollection interface, fs.ifsrmcollection__newenum, fsrm.ifsrmcollection__newenum, fsrm/IFsrmCollection::_NewEnum, fsrm/IFsrmCollection::get__NewEnum, get__NewEnum
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: FILTERED_DATA_SOURCES
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
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmCollection::get__NewEnum


## -description


Retrieves the <a href="_com_IUnknown">IUnknown</a> pointer of a new 
    <a href="https://msdn.microsoft.com/139e3c93-faef-4003-9079-e0e94494db3e">IEnumVARIANT</a> enumeration for the items in 
    the collection.

This property is read-only.


## -parameters


## -remarks



C/C++ users use this method to enumerate items in the collection. Call the 
    <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> of the 
    <a href="_com_IUnknown">IUnknown</a> interface to get the 
    <a href="https://msdn.microsoft.com/139e3c93-faef-4003-9079-e0e94494db3e">IEnumVARIANT</a> interface. Use the 
    <a href="https://msdn.microsoft.com/691c1624-8d01-41e0-890e-a4782eba1f59">IEnumVARIANT::Next</a> method to enumerate 
    the items of the collection. The items are returned as <b>VARIANT</b> values.

If the collection contains interfaces, the  variant type is <b>VT_DISPATCH</b>. Call the 
    <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> method on the 
    <b>pdispVal</b> member of the variant to get an interface to the specific object. For example, 
    if the collection contains report objects, you would query the <b>pdispVal</b> member for the 
    <a href="https://msdn.microsoft.com/2172a543-b3b7-453e-887b-05c8ee74f197">IFsrmReport</a> interface.

If the item is an <b>HRESULT</b> value, the variant type is 
    <b>VT_I4</b>. Use the <b>lVal</b> member of the variant to get the 
    <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/6a0c5d8b-5fed-4c55-971c-43430e3c6a8d">IFsrmCollection</a>
 

 

