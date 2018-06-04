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

# SHGLOBALCOUNTER enumeration


## -description


Identifiers for various global counters, or shared variables. Each global counter can be incremented or decremented using <a href="https://msdn.microsoft.com/088efa01-b070-4384-b17a-311aefb0737c">SHGlobalCounterIncrement</a> and <a href="https://msdn.microsoft.com/67b45cb9-9d8d-48ef-a7bc-9cd8824bdf2b">SHGlobalCounterDecrement</a>.


## -enum-fields




### -field GLOBALCOUNTER_SEARCHMANAGER

The global counter for use with the <a href="https://msdn.microsoft.com/23aeb0f6-857e-490c-9ede-11c0955a45c9">ISearchManager</a>.


### -field GLOBALCOUNTER_SEARCHOPTIONS

The global counter for use with <a href="https://msdn.microsoft.com/1e075961-63b7-4d91-b6ea-5d06d5b81140">ISearchQueryHelper</a> to identify whether a query parser's settings have changed.


### -field GLOBALCOUNTER_FOLDERSETTINGSCHANGE

The global counter used to identify whether folder settings have changed.


### -field GLOBALCOUNTER_RATINGS

The global counter used to identify whether ratings have changed.


### -field GLOBALCOUNTER_APPROVEDSITES

The global counter used to identify whether approved sites have changed.


### -field GLOBALCOUNTER_RESTRICTIONS

The global counter used to identify whether restrictions have changed.


### -field GLOBALCOUNTER_SHELLSETTINGSCHANGED

The global counter used to identify whether Shell settings have changed.


### -field GLOBALCOUNTER_SYSTEMPIDLCHANGE

The global counter used to identify whether a system PIDL has changed.


### -field GLOBALCOUNTER_OVERLAYMANAGER

The global counter used to identify whether the overlay manager state has changed.


### -field GLOBALCOUNTER_QUERYASSOCIATIONS

The global counter used to identify whether query associations have changed.


### -field GLOBALCOUNTER_IESESSIONS

The global counter used to identify whether the number of IE sessions has changed.


### -field GLOBALCOUNTER_IEONLY_SESSIONS

The global counter used to identify whether the number of IE sessions has changed.


### -field GLOBALCOUNTER_APPLICATION_DESTINATIONS

Identifies The global counter used to identify whether applications have been added or removed from the system.


### -field __UNUSED_RECYCLE_WAS_GLOBALCOUNTER_CSCSYNCINPROGRESS

Unused.


### -field GLOBALCOUNTER_BITBUCKETNUMDELETERS

The global counter used to identify deletions to the Recycle Bin.


### -field GLOBALCOUNTER_RECYCLEDIRTYCOUNT_SHARES

The global counter used to identify whether settings have changed on a share.


### -field GLOBALCOUNTER_RECYCLEDIRTYCOUNT_DRIVE_A

The global counter used to identify whether settings have changed on drive A.


### -field GLOBALCOUNTER_RECYCLEDIRTYCOUNT_DRIVE_B

The global counter used to identify whether settings have changed on drive B.


### -field GLOBALCOUNTER_RECYCLEDIRTYCOUNT_DRIVE_C

The global counter used to identify whether settings have changed on drive C.


### -field GLOBALCOUNTER_RECYCLEDIRTYCOUNT_DRIVE_D

The global counter used to identify whether settings have changed on drive D.


### -field GLOBALCOUNTER_RECYCLEDIRTYCOUNT_DRIVE_E

The global counter used to identify whether settings have changed on drive E.


### -field GLOBALCOUNTER_RECYCLEDIRTYCOUNT_DRIVE_F

The global counter used to identify whether settings have changed on drive F.


### -field GLOBALCOUNTER_RECYCLEDIRTYCOUNT_DRIVE_G

The global counter used to identify whether settings have changed on drive G.


### -field GLOBALCOUNTER_RECYCLEDIRTYCOUNT_DRIVE_H

The global counter used to identify whether settings have changed on drive H.


### -field GLOBALCOUNTER_RECYCLEDIRTYCOUNT_DRIVE_I

The global counter used to identify whether settings have changed on drive I.


### -field GLOBALCOUNTER_RECYCLEDIRTYCOUNT_DRIVE_J

The global counter used to identify whether settings have changed on drive J.


### -field GLOBALCOUNTER_RECYCLEDIRTYCOUNT_DRIVE_K

The global counter used to identify whether settings have changed on drive K.


### -field GLOBALCOUNTER_RECYCLEDIRTYCOUNT_DRIVE_L

The global counter used to identify whether settings have changed on drive L.


### -field GLOBALCOUNTER_RECYCLEDIRTYCOUNT_DRIVE_M

The global counter used to identify whether settings have changed on drive M.


### -field GLOBALCOUNTER_RECYCLEDIRTYCOUNT_DRIVE_N

The global counter used to identify whether settings have changed on drive N.


### -field GLOBALCOUNTER_RECYCLEDIRTYCOUNT_DRIVE_O

The global counter used to identify whether settings have changed on drive O.


### -field GLOBALCOUNTER_RECYCLEDIRTYCOUNT_DRIVE_P

The global counter used to identify whether settings have changed on drive P.


### -field GLOBALCOUNTER_RECYCLEDIRTYCOUNT_DRIVE_Q

The global counter used to identify whether settings have changed on drive Q.


### -field GLOBALCOUNTER_RECYCLEDIRTYCOUNT_DRIVE_R

The global counter used to identify whether settings have changed on drive R.


### -field GLOBALCOUNTER_RECYCLEDIRTYCOUNT_DRIVE_S

The global counter used to identify whether settings have changed on drive S.


### -field GLOBALCOUNTER_RECYCLEDIRTYCOUNT_DRIVE_T

The global counter used to identify whether settings have changed on drive T.


### -field GLOBALCOUNTER_RECYCLEDIRTYCOUNT_DRIVE_U

The global counter used to identify whether settings have changed on drive U.


### -field GLOBALCOUNTER_RECYCLEDIRTYCOUNT_DRIVE_V

The global counter used to identify whether settings have changed on drive V.


### -field GLOBALCOUNTER_RECYCLEDIRTYCOUNT_DRIVE_W

The global counter used to identify whether settings have changed on drive W.


### -field GLOBALCOUNTER_RECYCLEDIRTYCOUNT_DRIVE_X

The global counter used to identify whether settings have changed on drive X.


### -field GLOBALCOUNTER_RECYCLEDIRTYCOUNT_DRIVE_Y

The global counter used to identify whether settings have changed on drive Y.


### -field GLOBALCOUNTER_RECYCLEDIRTYCOUNT_DRIVE_Z

The global counter used to identify whether settings have changed on drive Z.


### -field __UNUSED_RECYCLE_WAS_GLOBALCOUNTER_RECYCLEDIRTYCOUNT_SERVERDRIVE

Unused.


### -field __UNUSED_RECYCLE_WAS_GLOBALCOUNTER_RECYCLEGLOBALDIRTYCOUNT

Unused.


### -field GLOBALCOUNTER_RECYCLEBINENUM

The global counter used to identify whether the Recycle Bin settings have changed.


### -field GLOBALCOUNTER_RECYCLEBINCORRUPTED

The global counter used to identify whether a Recycle Bin has been deleted.


### -field GLOBALCOUNTER_RATINGS_STATECOUNTER

The global counter used to identify whether ratings have changed.


### -field GLOBALCOUNTER_PRIVATE_PROFILE_CACHE

The global counter state.


### -field GLOBALCOUNTER_INTERNETTOOLBAR_LAYOUT

The global counter used to identify whether the Internet toolbar layout has changed.


### -field GLOBALCOUNTER_FOLDERDEFINITION_CACHE

The global counter used to identify changes to the folder definition cache.


### -field GLOBALCOUNTER_COMMONPLACES_LIST_CACHE

The global counter used to identify state changes for the commonplaces list cache.


### -field GLOBALCOUNTER_PRIVATE_PROFILE_CACHE_MACHINEWIDE

The global counter state, machine-wide.


### -field GLOBALCOUNTER_ASSOCCHANGED

The global counter used to identify the current GlobalAssocChangedCounter registry value for HKEY_LOCAL_MACHINE\Software\Microsoft\Windows\CurrentVersion\Explorer.
                    


### -field GLOBALCOUNTER_APP_ITEMS_STATE_STORE_CACHE

<b>Introduced in Windows 8</b>. The global counter used to identify whether the Store is current.


### -field GLOBALCOUNTER_SETTINGSYNC_ENABLED

<b>Introduced in Windows 8</b>. The global counter used to determine whether sync is enabled or disabled.


### -field GLOBALCOUNTER_APPSFOLDER_FILETYPEASSOCIATION_COUNTER

<b>Introduced in Windows 8</b>. The global counter used to identify the current FTACounter registry value for HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\ImmersiveShell\StateStore.


### -field GLOBALCOUNTER_USERINFOCHANGED

<b>Introduced in Windows 8</b>. The global counter used to identify user info change state.


### -field GLOBALCOUNTER_SYNC_ENGINE_INFORMATION_CACHE_MACHINEWIDE

<b>Introduced in Windows 8.1</b>. The global counter used to identify sync engine counter state, machine wide..


### -field GLOBALCOUNTER_BANNERS_DATAMODEL_CACHE_MACHINEWIDE


### -field GLOBALCOUNTER_MAXIMUMVALUE

The maximum value any shared variable can have.


## -remarks



These global counters are shared variables that can help identify whether the state of a Windows component has changed over time. They can be used with these functions: <a href="https://msdn.microsoft.com/67b45cb9-9d8d-48ef-a7bc-9cd8824bdf2b">SHGlobalCounterDecrement</a>, <a href="https://msdn.microsoft.com/088efa01-b070-4384-b17a-311aefb0737c">SHGlobalCounterIncrement</a>, <a href="https://msdn.microsoft.com/cf158770-c9af-4488-9ed0-486e9a528a65">SHGlobalCounterGetValue</a>.

<h3><a id="Example"></a><a id="example"></a><a id="EXAMPLE"></a>Example</h3>
The following pseudocode example shows how a global counter can be used.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>void ValidateSomeSettings()
    {
        // Get the current GLOBALCOUNTER_SHELLSETTINGSCHANGED value.
        long lGlobalSettingsCounter = SHGlobalCounterGetValue(GLOBALCOUNTER_SHELLSETTINGSCHANGED);
            
        // Do some other work
        ...
    
        // Verify whether the Shell settings have changed since entering this method.
        if (lGlobalSettingsCounter == SHGlobalCounterGetValue(GLOBALCOUNTER_SHELLSETTINGSCHANGED))
        {
            // Commit the work that was done earlier 
            ...
        }
    
        else
        {
            // Shell settings have changed. Rollback and redo.
            ...
        }
    }</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/67b45cb9-9d8d-48ef-a7bc-9cd8824bdf2b">SHGlobalCounterDecrement</a>



<a href="https://msdn.microsoft.com/cf158770-c9af-4488-9ed0-486e9a528a65">SHGlobalCounterGetValue</a>



<a href="https://msdn.microsoft.com/088efa01-b070-4384-b17a-311aefb0737c">SHGlobalCounterIncrement</a>
 

 

