---
UID: NF:coml2api.StgCreatePropStg
title: StgCreatePropStg function
author: windows-sdk-content
description: Creates and opens a property set in a specified storage or stream object.
old-location: stg\stgcreatepropstg.htm
tech.root: stg
ms.assetid: fc171888-3723-4894-a356-1b234352c4e8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: StgCreatePropStg, StgCreatePropStg function [Structured Storage], _stg_stgcreatepropstg, coml2api/StgCreatePropStg, stg.stgcreatepropstg
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: coml2api.h
req.include-header: Propidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-Core-Com-l2-1-1.dll
 - coml2.dll
api_name:
 - StgCreatePropStg
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# StgCreatePropStg function


## -description


The <b>StgCreatePropStg</b> function creates and opens a property set in a specified storage or stream object. The property set supplies the system-provided, stand-alone implementation of the 
<a href="https://msdn.microsoft.com/c021f695-db54-4861-9f30-35a81d2dccd5">IPropertyStorage</a> interface.


## -parameters




### -param pUnk [in]

A pointer to the <b>IUnknown</b> interface on the storage or stream object that stores the new property set.


### -param fmtid [in]

The FMTID of the property set to be created.


### -param pclsid [in]

A Pointer to the initial CLSID for this property set. May be <b>NULL</b>, in which case <i>pclsid</i> is set to all zeroes.


### -param grfFlags [in]

The values from <a href="https://msdn.microsoft.com/6f865c8f-bbca-4122-b076-14f2bc56f292">PROPSETFLAG Constants</a> that determine how the property set is created and opened.


### -param dwReserved [in]

Reserved; must be zero.


### -param ppPropStg [out]

The address of an 
<a href="https://msdn.microsoft.com/c021f695-db54-4861-9f30-35a81d2dccd5">IPropertyStorage</a>* pointer variable that receives the interface pointer to the new property set.


## -returns



This function supports the standard return values E_INVALIDARG and E_UNEXPECTED, in addition to the following:




## -remarks



<b>StgCreatePropStg</b> creates and opens a new property set which supplies the system-provided, stand-alone implementation of the 
<a href="https://msdn.microsoft.com/c021f695-db54-4861-9f30-35a81d2dccd5">IPropertyStorage</a> interface. The new property set is contained in the storage or stream object specified by <i>pUnk</i>. The value of the <i>grfFlags</i> parameter indicates whether <i>pUnk</i> specifies a storage or stream object. For example, if PROPSETFLAG_NONSIMPLE is set, then <i>pUnk</i> can be queried for an 
<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> interface on a storage object.

In either case, this function calls <i>pUnk-&gt;AddRef</i> for the storage or stream object containing the property set. It is the responsibility of the caller to release the object when it is no longer needed.

This function is similar to the <a href="https://msdn.microsoft.com/9307788d-bce6-4025-8043-8b68e874a62b">IPropertySetStorage::Create</a> method. However, 
<b>StgCreatePropStg</b> adds the <i>pUnk</i> parameter and supports the PROPSETFLAG_UNBUFFERED value for the <i>grfFlags</i> parameter. Use this function instead of the 
<b>Create</b> method if you have an 
<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> interface that does not support the 
<a href="https://msdn.microsoft.com/0ea3e1e0-c135-4138-81e4-f72412fc3128">IPropertySetStorage</a> interface, or if you want to use the PROPSETFLAG_UNBUFFERED value. For more information about using this PROPSETFLAG_UNBUFFERED enumeration value, see <a href="https://msdn.microsoft.com/6f865c8f-bbca-4122-b076-14f2bc56f292">PROPSETFLAG Constants</a>.

The property set automatically contains code page and locale identifier (ID) properties. These are set to the current system default and the current user default, respectively.

The <i>grfFlags</i> parameter is a combination of values taken from <a href="https://msdn.microsoft.com/6f865c8f-bbca-4122-b076-14f2bc56f292">PROPSETFLAG Constants</a>. The new enumeration value PROPSETFLAG_UNBUFFERED is supported. For more information, see <b>PROPSETFLAG Constants</b>.

This function is exported out of the redistributable Iprop.dll, which is included in Windows NT 4.0 with Service Pack 2 (SP2) and later and available as a redistributable in Windows 95, Windows 98 and later. In Windows 2000 and Windows XP, it is exported out of ole32.dll. It can also be exported out of iprop.dll in Windows 2000 and Windows XP, but the call gets forwarded to ole32.dll.




## -see-also




<a href="https://msdn.microsoft.com/0ea3e1e0-c135-4138-81e4-f72412fc3128">IPropertySetStorage</a>



<a href="https://msdn.microsoft.com/0ea5aadf-0b3f-44ac-9bb7-a7e8292f04c2">IPropertySetStorage-Stand-alone Implementation</a>



<a href="https://msdn.microsoft.com/c021f695-db54-4861-9f30-35a81d2dccd5">IPropertyStorage</a>



<a href="https://msdn.microsoft.com/8de32538-de11-4e4d-9269-145b2accb099">IPropertyStorage-Stand-alone Implementation</a>



<a href="https://msdn.microsoft.com/6f865c8f-bbca-4122-b076-14f2bc56f292">PROPSETFLAG Constants</a>



<a href="https://msdn.microsoft.com/0113b29d-23aa-4590-b8ac-33789a7a2ed4">StgCreatePropSetStg</a>



<a href="https://msdn.microsoft.com/ecc78e49-f1c2-4c2d-8390-b2b6f1dc776e">StgOpenPropStg</a>
 

 

