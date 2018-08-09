---
UID: NF:faxcom.IFaxTiff.get_RecipientNumber
title: IFaxTiff::get_RecipientNumber
author: windows-sdk-content
description: Retrieves the RecipientNumber property for a FaxTiff object. The RecipientNumber property is a null-terminated string that contains the fax number to which a fax was transmitted.
old-location: fax\_mfax_ifaxtiff_get_recipientnumber_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_3b8y.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: FaxTiff object [Fax Service],RecipientNumber property, FaxTiff.RecipientNumber, IFaxTiff.get_RecipientNumber, IFaxTiff::get_RecipientNumber, RecipientNumber property [Fax Service], RecipientNumber property [Fax Service],FaxTiff object, _mfax_ifaxtiff_get_recipientnumber, fax._mfax_ifaxtiff_get_recipientnumber, fax._mfax_ifaxtiff_get_recipientnumber_vb, get_RecipientNumber
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: faxcom.h
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
tech.root: 
req.typenames: ShellWindowTypeConstants
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Faxcom.dll
api_name:
 - FaxTiff.RecipientNumber
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxTiff::get_RecipientNumber


## -description


Retrieves the <b>RecipientNumber</b> property for a <a href="https://msdn.microsoft.com/en-us/library/ms691832(v=VS.85).aspx">FaxTiff</a> object. The <b>RecipientNumber</b> property is a null-terminated string that contains the fax number to which a fax was transmitted.

This property is read-only.


## -parameters


## -remarks



A fax client application must  set the <a href="https://msdn.microsoft.com/en-us/library/ms690773(v=VS.85).aspx">Image</a> property before retrieving another property for a <a href="https://msdn.microsoft.com/en-us/library/ms691832(v=VS.85).aspx">FaxTiff</a> object.

The <b>RecipientNumber</b> property has meaning only for outbound fax transmissions. This is because the <a href="https://msdn.microsoft.com/library/windows/hardware/dn922691">Csid</a> property and the <b>RecipientNumber</b> property are identical for inbound faxes.

The <b>get_RecipientNumber</b> method sets the <i>pVal</i> parameter to the fax number of the fax recipient, if it is available. If the information is not available, the method returns "Unavailable".

The <b>RecipientNumber</b> property is a string that represents the fax number of the fax recipient, if it is available. If the information is not available, <b>RecipientNumber</b> is an empty string.

The <b>get_RecipientNumber</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn922691">Csid</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690285(v=VS.85).aspx">FaxTiff</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691802(v=VS.85).aspx">IFaxTiff</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690773(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a>
 

 

