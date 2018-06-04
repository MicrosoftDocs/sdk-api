---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# __MIDL___MIDL_itf_vsmgmt_0000_0000_0001 structure


## -description


The <a href="base.vss_mgmt_object">VSS_MGMT_OBJECT_UNION</a> union 
    is a union of <a href="https://msdn.microsoft.com/f17765d5-ccb4-4ede-86e4-36ac80022da0">VSS_VOLUME_PROP</a>, 
    <a href="https://msdn.microsoft.com/c4a20583-7fee-4ae1-97ed-d80b2a7539e3">VSS_DIFF_VOLUME_PROP</a>, and 
    <a href="https://msdn.microsoft.com/9627d7b0-e9d0-425f-9051-cf4ab6b75a8c">VSS_DIFF_AREA_PROP</a> structures determined by the 
    <b>Type</b> member of the 
    <a href="https://msdn.microsoft.com/86681207-969e-4b33-aff8-79454ab04829">VSS_MGMT_OBJECT_PROP</a> structure containing this 
    union.


## -struct-fields




### -field Vol

If the <b>Type</b> member of the 
      <a href="https://msdn.microsoft.com/86681207-969e-4b33-aff8-79454ab04829">VSS_MGMT_OBJECT_PROP</a> structure containing this 
      union is <b>VSS_MGMT_OBJECT_VOLUME</b>, then this union is a 
      <a href="https://msdn.microsoft.com/f17765d5-ccb4-4ede-86e4-36ac80022da0">VSS_VOLUME_PROP</a> structure.


### -field DiffVol

If the <b>Type</b> member of the 
      <a href="https://msdn.microsoft.com/86681207-969e-4b33-aff8-79454ab04829">VSS_MGMT_OBJECT_PROP</a> structure containing this 
      union is <b>VSS_MGMT_OBJECT_DIFF_VOLUME</b>, then this union is 
      a <a href="https://msdn.microsoft.com/c4a20583-7fee-4ae1-97ed-d80b2a7539e3">VSS_DIFF_VOLUME_PROP</a> structure.


### -field DiffArea

If the <b>Type</b> member of the 
      <a href="https://msdn.microsoft.com/86681207-969e-4b33-aff8-79454ab04829">VSS_MGMT_OBJECT_PROP</a> structure containing this 
      union is <b>VSS_MGMT_OBJECT_DIFF_AREA</b>, then this union is a 
      <a href="https://msdn.microsoft.com/9627d7b0-e9d0-425f-9051-cf4ab6b75a8c">VSS_DIFF_AREA_PROP</a> structure.


## -remarks



The <a href="base.vss_mgmt_object">VSS_MGMT_OBJECT_UNION</a> structure is used only as a 
    member of the <a href="https://msdn.microsoft.com/86681207-969e-4b33-aff8-79454ab04829">VSS_MGMT_OBJECT_PROP</a> 
    structure.

Applications need to consult the <b>Type</b> member of 
    <a href="https://msdn.microsoft.com/86681207-969e-4b33-aff8-79454ab04829">VSS_MGMT_OBJECT_PROP</a> to determine whether the 
    <a href="base.vss_mgmt_object">VSS_MGMT_OBJECT_UNION</a> contains a 
    <a href="https://msdn.microsoft.com/f17765d5-ccb4-4ede-86e4-36ac80022da0">VSS_VOLUME_PROP</a>, 
    <a href="https://msdn.microsoft.com/c4a20583-7fee-4ae1-97ed-d80b2a7539e3">VSS_DIFF_VOLUME_PROP</a>, or 
    <a href="https://msdn.microsoft.com/9627d7b0-e9d0-425f-9051-cf4ab6b75a8c">VSS_DIFF_AREA_PROP</a> object.

When a <a href="base.vss_mgmt_object">VSS_MGMT_OBJECT_UNION</a> structure has been returned 
    by a member method of a COM interface (from, for example, 
    <a href="https://msdn.microsoft.com/0ddcf25d-dc3e-4522-a98e-98d867230d42">IVssEnumMgmtObject::Next</a>), an application 
    must call <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> for every string and byte array 
    value contained in its constituent structure 
    (<a href="https://msdn.microsoft.com/f17765d5-ccb4-4ede-86e4-36ac80022da0">VSS_VOLUME_PROP</a>, 
    <a href="https://msdn.microsoft.com/c4a20583-7fee-4ae1-97ed-d80b2a7539e3">VSS_DIFF_VOLUME_PROP</a>, or 
    <a href="https://msdn.microsoft.com/9627d7b0-e9d0-425f-9051-cf4ab6b75a8c">VSS_DIFF_AREA_PROP</a>).




## -see-also




<a href="https://msdn.microsoft.com/0ddcf25d-dc3e-4522-a98e-98d867230d42">IVssEnumMgmtObject::Next</a>



<a href="https://msdn.microsoft.com/9627d7b0-e9d0-425f-9051-cf4ab6b75a8c">VSS_DIFF_AREA_PROP</a>



<a href="https://msdn.microsoft.com/c4a20583-7fee-4ae1-97ed-d80b2a7539e3">VSS_DIFF_VOLUME_PROP</a>



<a href="https://msdn.microsoft.com/ea28ff2c-6603-4193-9d5f-b41fffe28a90">VSS_MGMT_OBJECT_TYPE</a>



<a href="https://msdn.microsoft.com/f17765d5-ccb4-4ede-86e4-36ac80022da0">VSS_VOLUME_PROP</a>



<a href="https://msdn.microsoft.com/20cf12e4-4611-4e39-9f6f-e29f15e58b36">Volume Shadow Copy API Structures</a>
 

 

