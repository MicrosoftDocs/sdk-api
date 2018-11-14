---
UID: NF:coml2api.StgOpenPropStg
title: StgOpenPropStg function
author: windows-sdk-content
description: Opens a specified property set in a specified storage or stream object.
old-location: stg\stgopenpropstg.htm
tech.root: Stg
ms.assetid: ecc78e49-f1c2-4c2d-8390-b2b6f1dc776e
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: StgOpenPropStg, StgOpenPropStg function [Structured Storage], _stg_stgopenpropstg, coml2api/StgOpenPropStg, stg.stgopenpropstg
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
 - StgOpenPropStg
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- StgOpenPropStg
: 
---

# StgOpenPropStg function


## -description


The <b>StgOpenPropStg</b> function opens a specified property set in a specified storage or stream object. The property set supplies the system-provided, stand-alone implementation of the 
<a href="https://msdn.microsoft.com/en-us/library/Aa379968(v=VS.85).aspx">IPropertyStorage</a> interface.


## -parameters




### -param pUnk [in]

The interface pointer for <b>IUnknown</b> interface on the storage or stream object that contains the requested property set object.


### -param fmtid [in]

The FMTID of the property set to be opened.


### -param grfFlags [in]

The values from <a href="https://msdn.microsoft.com/en-us/library/Aa380069(v=VS.85).aspx">PROPSETFLAG Constants</a>.


### -param dwReserved [in]

Reserved for future use; must be zero.


### -param ppPropStg [out]

A pointer to 
an <a href="https://msdn.microsoft.com/en-us/library/Aa379968(v=VS.85).aspx">IPropertyStorage</a>* pointer variable that receives the interface pointer to the requested property set.


## -returns



This function supports the standard return values E_INVALIDARG and E_UNEXPECTED, in addition to the following:




## -remarks



<b>StgOpenPropStg</b> opens the requested property set and supplies the system-provided, stand-alone implementation of the 
<a href="https://msdn.microsoft.com/en-us/library/Aa379968(v=VS.85).aspx">IPropertyStorage</a> interface. The requested property set is contained in the storage or stream object specified by <i>pUnk</i>. The value of the <i>grfFlags</i> parameter indicates whether <i>pUnk</i> specifies a storage or stream object. For example, if PROPSETFLAG_NONSIMPLE is set, then <i>pUnk</i> can be queried for an 
<a href="https://msdn.microsoft.com/en-us/library/Aa380015(v=VS.85).aspx">IStorage</a> interface on a storage object.

In either case, this function calls <i>pUnk-&gt;AddRef</i> for the storage or stream object containing the property set. The caller must release the object when no longer required.

This function is similar to the <a href="https://msdn.microsoft.com/en-us/library/Aa379965(v=VS.85).aspx">IPropertySetStorage::Open</a> method. However, 
<b>StgOpenPropStg</b> adds the <i>pUnk</i> and <i>grfFlags</i> parameters, including the PROPSETFLAG_UNBUFFERED value for the <i>grfFlags</i> parameter. Use this function instead of the 
Open method if you have an 
<a href="https://msdn.microsoft.com/en-us/library/Aa380015(v=VS.85).aspx">IStorage</a> interface that does not support the 
<a href="https://msdn.microsoft.com/en-us/library/Aa379840(v=VS.85).aspx">IPropertySetStorage</a> interface, or if you want to use the PROPSETFLAG_UNBUFFERED value. For more information about using PROPSETFLAG_UNBUFFERED, see <a href="https://msdn.microsoft.com/en-us/library/Aa380069(v=VS.85).aspx">PROPSETFLAG Constants</a>.

The <i>grfFlags</i> parameter is a combination of values taken from <a href="https://msdn.microsoft.com/en-us/library/Aa380069(v=VS.85).aspx">PROPSETFLAG Constants</a>. The new enumeration value PROPSETFLAG_UNBUFFERED is supported. For more information, see 
<b>PROPSETFLAG Constants</b>.

This function is exported out of the redistributable iprop.dll, which is included in Windows NT 4.0 with Service Pack 2 (SP2) and available as a redistributable in Windows 95 and later. In Windows 2000, it is exported out of Ole32.dll. It can also be exported out of iprop.dll in Windows 2000, but the call gets forwarded to ole32.dll.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa379840(v=VS.85).aspx">IPropertySetStorage</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa379966(v=VS.85).aspx">IPropertySetStorage-Stand-alone Implementation</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa379968(v=VS.85).aspx">IPropertyStorage</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa379983(v=VS.85).aspx">IPropertyStorage-Stand-alone Implementation</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380069(v=VS.85).aspx">PROPSETFLAG Constants</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380325(v=VS.85).aspx">StgCreatePropSetStg</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380327(v=VS.85).aspx">StgCreatePropStg</a>
 

 

