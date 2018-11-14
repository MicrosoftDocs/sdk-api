---
UID: NC:rasdlg.RASPBDLGFUNCW
title: RASPBDLGFUNCW
author: windows-sdk-content
description: The RasPBDlgFunc function is an application-defined callback function that receives notifications of user activity while the RasPhonebookDlg dialog box is open.
old-location: rras\raspbdlgfunc.htm
tech.root: rras
ms.assetid: 70bb60a1-6a56-43fd-9352-8ced34ddd174
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: RASPBDEVENT_AddEntry, RASPBDEVENT_DialEntry, RASPBDEVENT_EditEntry, RASPBDEVENT_EditGlobals, RASPBDEVENT_NoUser, RASPBDEVENT_NoUserEdit, RASPBDEVENT_RemoveEntry, RasPBDlgFunc, RasPBDlgFunc callback, RasPBDlgFunc callback function [RAS], RasPBDlgFuncA, RasPBDlgFuncW, _ras_raspbdlgfunc, rasdlg/RasPBDlgFunc, rasdlg/RasPBDlgFuncA, rasdlg/RasPBDlgFuncW, rras.raspbdlgfunc
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: rasdlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RasPBDlgFuncW (Unicode) and RasPBDlgFuncA (ANSI)
req.idl: 
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
 - UserDefined
api_location:
 - Rasdlg.h
api_name:
 - RasPBDlgFunc
 - RasPBDlgFuncA
 - RasPBDlgFuncW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RASPBDLGFUNCW callback function


## -description


The 
<b>RasPBDlgFunc</b> function is an application-defined callback function that receives notifications of user activity while the 
<a href="https://msdn.microsoft.com/64603090-ec03-4eac-9da6-cb631c97dfb5">RasPhonebookDlg</a> dialog box is open.


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3


### -param Arg4








#### - dwCallbackId [in]

Specifies the application-defined value that was specified in the <b>dwCallback</b> member of the 
<a href="https://msdn.microsoft.com/fa5843ec-1f39-40b2-8c5a-9b72f3cc3539">RASPBDLG</a> structure passed to the 
<a href="https://msdn.microsoft.com/64603090-ec03-4eac-9da6-cb631c97dfb5">RasPhonebookDlg</a> function.


#### - dwEvent [in]

A set of bit flags that specifies the event that occurred. This parameter is one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RASPBDEVENT_AddEntry"></a><a id="raspbdevent_addentry"></a><a id="RASPBDEVENT_ADDENTRY"></a><dl>
<dt><b>RASPBDEVENT_AddEntry</b></dt>
</dl>
</td>
<td width="60%">
Received when the user creates a new phone-book entry or copies an existing phone-book entry. The <i>pszText</i> parameter is the name of the new or copied entry. The <i>pData</i> parameter is undefined.

</td>
</tr>
<tr>
<td width="40%"><a id="RASPBDEVENT_EditEntry"></a><a id="raspbdevent_editentry"></a><a id="RASPBDEVENT_EDITENTRY"></a><dl>
<dt><b>RASPBDEVENT_EditEntry</b></dt>
</dl>
</td>
<td width="60%">
Received when the user changes an existing phone-book entry. The <i>pszText</i> parameter is the name of the modified entry. The <i>pData</i> parameter is undefined.

</td>
</tr>
<tr>
<td width="40%"><a id="RASPBDEVENT_RemoveEntry"></a><a id="raspbdevent_removeentry"></a><a id="RASPBDEVENT_REMOVEENTRY"></a><dl>
<dt><b>RASPBDEVENT_RemoveEntry</b></dt>
</dl>
</td>
<td width="60%">
Received when the user deletes a phone-book entry. The <i>pszText</i> parameter is the name of the deleted entry. The <i>pData</i> parameter is undefined.

</td>
</tr>
<tr>
<td width="40%"><a id="RASPBDEVENT_DialEntry"></a><a id="raspbdevent_dialentry"></a><a id="RASPBDEVENT_DIALENTRY"></a><dl>
<dt><b>RASPBDEVENT_DialEntry</b></dt>
</dl>
</td>
<td width="60%">
Received when the user successfully dials an entry. The <i>pszText</i> parameter is the name of the newly connected entry. The <i>pData</i> parameter is undefined.

</td>
</tr>
<tr>
<td width="40%"><a id="RASPBDEVENT_EditGlobals"></a><a id="raspbdevent_editglobals"></a><a id="RASPBDEVENT_EDITGLOBALS"></a><dl>
<dt><b>RASPBDEVENT_EditGlobals</b></dt>
</dl>
</td>
<td width="60%">
Received when the user makes changes in the<b> User Preferences</b> property sheet. The <i>pszText</i> parameter is the full path of the default phone-book file selected by the user. The <i>pData</i> parameter is undefined. 




This event is also received during dialog startup if the <i>lpszPhonebook</i> parameter of the 
<a href="https://msdn.microsoft.com/64603090-ec03-4eac-9da6-cb631c97dfb5">RasPhonebookDlg</a> call is <b>NULL</b>. In this case, the event informs the caller of the path of the default phone book.

</td>
</tr>
<tr>
<td width="40%"><a id="RASPBDEVENT_NoUser"></a><a id="raspbdevent_nouser"></a><a id="RASPBDEVENT_NOUSER"></a><dl>
<dt><b>RASPBDEVENT_NoUser</b></dt>
</dl>
</td>
<td width="60%">
Received during dialog box initialization when the RASPBDFLAG_NoUser flag is set. The <i>pData</i> parameter is a pointer to a 
<a href="https://msdn.microsoft.com/a75d74e1-5a4b-4a17-9665-c964a9a28049">RASNOUSER</a> structure. The callback function should fill the structure with the user's logon credentials and dialog time out. The 
<a href="https://msdn.microsoft.com/64603090-ec03-4eac-9da6-cb631c97dfb5">RasPhonebookDlg</a> function then uses the supplied credentials for authentication by the remote server. The <i>pszText</i> parameter is undefined.

</td>
</tr>
<tr>
<td width="40%"><a id="RASPBDEVENT_NoUserEdit"></a><a id="raspbdevent_nouseredit"></a><a id="RASPBDEVENT_NOUSEREDIT"></a><dl>
<dt><b>RASPBDEVENT_NoUserEdit</b></dt>
</dl>
</td>
<td width="60%">
Received if the RASPBDFLAG_NoUser flag is set and the user changes the credentials that are supplied during the <b>RASPBDEVENT_NoUser</b> event. The <i>pData</i> parameter is a pointer to the 
<a href="https://msdn.microsoft.com/a75d74e1-5a4b-4a17-9665-c964a9a28049">RASNOUSER</a> structure that contains the updated credentials. This occurs during a dialing operation if the user changes his or her password, or if the authentication fails and the user retries authentication with different credentials. The <i>pszText</i> parameter is undefined.

</td>
</tr>
</table>
 


#### - pData [in]

Pointer to an additional buffer argument whose meaning depends on the event indicated in the <i>dwEvent</i> parameter.


#### - pszText [in]

Pointer to an additional string argument whose meaning depends on the event indicated in the <i>dwEvent</i> parameter.


## -returns



This callback function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/a75d74e1-5a4b-4a17-9665-c964a9a28049">RASNOUSER</a>



<a href="https://msdn.microsoft.com/64603090-ec03-4eac-9da6-cb631c97dfb5">RasPhonebookDlg</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/5883a77a-6af8-47a8-bb28-6ef60a5aa2f1">Remote Access Service Functions</a>
 

 

