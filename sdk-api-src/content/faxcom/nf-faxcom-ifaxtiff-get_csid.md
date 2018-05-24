---
UID: NF:faxcom.IFaxTiff.get_Csid
title: IFaxTiff::get_Csid
author: windows-driver-content
description: Retrieves the Csid property for a FaxTiff object. The Csid property is a string that contains called station identifier (CSID) information, which is typically the fax number of the device that received the specified fax file.
old-location: fax\_mfax_ifaxtiff_get_csid_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_2ask.htm
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: Csid property [Fax Service], Csid property [Fax Service],FaxTiff object, FaxTiff object [Fax Service],Csid property, FaxTiff.Csid, IFaxTiff.get_Csid, IFaxTiff::get_Csid, _mfax_ifaxtiff_get_csid, fax._mfax_ifaxtiff_get_csid, fax._mfax_ifaxtiff_get_csid_vb, get_Csid
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: ShellWindowTypeConstants
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Faxcom.dll
api_name:
-	FaxTiff.Csid
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxTiff::get_Csid


## -description


Retrieves the <b>Csid</b> property for a <a href="https://msdn.microsoft.com/70acd518-4058-4146-bbdf-50108d0c7e3f">FaxTiff</a> object. The <b>Csid</b> property is a string that contains called station identifier (CSID) information, which is typically the fax number of the device that received the specified fax file.

This property is read-only.


## -parameters


## -remarks



A fax client application must  set the <a href="https://msdn.microsoft.com/9e41ae1f-070d-4365-9d6a-a37f1979dae7">Image</a> property before retrieving another property for a <a href="https://msdn.microsoft.com/70acd518-4058-4146-bbdf-50108d0c7e3f">FaxTiff</a> object.

The <b>get_Csid</b> method sets the <i>pVal</i> parameter to the string that identifies the called device, if that information is available. If the information is not available, the method returns "Unavailable".

The <b>Csid</b> property is a string that identifies the called device, if that information is available. If the information is not available, <b>Csid</b> is an empty string.

The <b>get_Csid</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/a8371d98-8a66-484a-9179-4894ae0a7dfc">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/98d385be-cebb-428e-92f7-22a1fc814c3c">FaxTiff</a>



<a href="https://msdn.microsoft.com/a4c46893-502d-4d5c-a895-837cffc014e4">IFaxTiff</a>



<a href="https://msdn.microsoft.com/9e41ae1f-070d-4365-9d6a-a37f1979dae7">Image</a>



<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a>
 

 

